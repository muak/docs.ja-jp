---
title: 非同期タスクのキャンセル後、一定期間 (Visual Basic)
ms.date: 07/20/2015
ms.assetid: a48045a3-6a99-42af-b824-af340f0b9a5d
ms.openlocfilehash: b1c56cb6d894dbcd9e70f06d7e5cd44b559b8cd4
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2018
ms.locfileid: "50033702"
---
# <a name="cancel-async-tasks-after-a-period-of-time-visual-basic"></a>非同期タスクのキャンセル後、一定期間 (Visual Basic)
<xref:System.Threading.CancellationTokenSource.CancelAfter%2A?displayProperty=nameWithType> メソッドを使用すると、一定の時間が過ぎた後に非同期操作が完了するまで待たない場合に、その操作を取り消しできます。 このメソッドは、`CancelAfter` 式によって指定された時間内に完了しない、関連付けられたタスクの取り消しをスケジュールします。  
  
 この例で開発されたコードに追加[非同期タスクまたはタスクの一覧 (Visual Basic) をキャンセル](../../../../visual-basic/programming-guide/concepts/async/cancel-an-async-task-or-a-list-of-tasks.md)web サイトの一覧をダウンロードして、それぞれのコンテンツの長さを表示します。  
  
> [!NOTE]
>  例を実行するには、Visual Studio 2012 以降と .NET Framework 4.5 が必要または後でコンピューターにインストールされています。  
  
## <a name="downloading-the-example"></a>例をダウンロードする  
 完全な Windows Presentation Foundation (WPF) プロジェクトは「[Async Sample: Fine Tuning Your Application (非同期のサンプル: アプリケーションの微調整)](https://code.msdn.microsoft.com/Async-Fine-Tuning-Your-a676abea)」からダウンロードできます。ダウンロード後、次の手順に従います。  
  
1.  ダウンロードしたファイルを圧縮解除し、Visual Studio を起動します。  
  
2.  メニュー バーで **[ファイル]**、 **[開く]**、 **[プロジェクト/ソリューション]** の順に選択します。  
  
3.  **プロジェクトを開く** ダイアログ ボックスでは、圧縮を解除するには、サンプル コードを保持するフォルダーを開き、AsyncFineTuningVB のソリューション (.sln) ファイルを開きます。  
  
4.  **ソリューション エクスプローラー**で、**CancelAfterTime** プロジェクトのショートカット メニューを開き、**[スタートアップ プロジェクトに設定]** をクリックします。  
  
5.  F5 キーを押してプロジェクトを実行します。  
  
     Ctrl + F5 キーを押して、デバッグを行わずにプロジェクトを実行します。  
  
6.  プログラムを複数回実行して、出力がすべての Web サイトの出力を示したり、どの Web サイトの出力も示さなかったり、一部の Web サイトの出力を示したりすることを確認します。  
  
 プロジェクトをダウンロードしない場合は、このトピックの最後の MainWindow.xaml.vb ファイルを確認できます。  
  
## <a name="building-the-example"></a>例のビルド  
 このトピックの例で開発されたプロジェクトに追加します[非同期タスクまたはタスクの一覧 (Visual Basic) をキャンセル](../../../../visual-basic/programming-guide/concepts/async/cancel-an-async-task-or-a-list-of-tasks.md)タスクの一覧をキャンセルします。 この例では、**[キャンセル]** ボタンは明示的に使用していませんが、同じ UI を使用します。  
  
 この例を自分で 1 つずつビルドするには、"例をダウンロードする" セクションの手順に従います。ただし、**[スタートアップ プロジェクト]** として **CancelAListOfTasks** を選択します。 そのプロジェクトに、このトピックでの変更を追加します。  
  
 次の例に示すように、タスクが取り消し済みとマークされるまでの最大時間を指定するには、`CancelAfter` に `startButton_Click` への呼び出しを追加します。 追加部分にはアスタリスクが付いています。  
  
```vb  
Private Async Sub startButton_Click(sender As Object, e As RoutedEventArgs)  
  
    ' Instantiate the CancellationTokenSource.  
    cts = New CancellationTokenSource()  
  
    resultsTextBox.Clear()  
  
    Try  
        ' ***Set up the CancellationTokenSource to cancel after 2.5 seconds. (You   
        ' can adjust the time.)  
        cts.CancelAfter(2500)  
  
        Await AccessTheWebAsync(cts.Token)  
        resultsTextBox.Text &= vbCrLf & "Downloads complete."  
  
    Catch ex As OperationCanceledException  
        resultsTextBox.Text &= vbCrLf & "Downloads canceled." & vbCrLf  
  
    Catch ex As Exception  
        resultsTextBox.Text &= vbCrLf & "Downloads failed." & vbCrLf  
    End Try  
  
    ' Set the CancellationTokenSource to Nothing when the download is complete.  
    cts = Nothing  
End Sub  
```  
  
 プログラムを複数回実行して、出力がすべての Web サイトの出力を示したり、どの Web サイトの出力も示さなかったり、一部の Web サイトの出力を示したりすることを確認します。 出力例を次に示します。  
  
```  
Length of the downloaded string: 35990.  
  
Length of the downloaded string: 407399.  
  
Length of the downloaded string: 226091.  
  
Downloads canceled.  
```  
  
## <a name="complete-example"></a>コード例全体  
 次のコードは、例では、MainWindow.xaml.vb ファイルの完全なテキストです。 アスタリスクはこの例のために追加された要素を示しています。  
  
 <xref:System.Net.Http> の参照を追加する必要があることに注意してください。  
  
 このプロジェクトは「[Async Sample: Fine Tuning Your Application (非同期のサンプル: アプリケーションの微調整)](https://code.msdn.microsoft.com/Async-Fine-Tuning-Your-a676abea)」からダウンロードできます。  
  
```vb  
' Add an Imports directive and a reference for System.Net.Http.  
Imports System.Net.Http  
  
' Add the following Imports directive for System.Threading.  
Imports System.Threading  
  
Class MainWindow  
  
    ' Declare a System.Threading.CancellationTokenSource.  
    Dim cts As CancellationTokenSource  
  
    Private Async Sub startButton_Click(sender As Object, e As RoutedEventArgs)  
  
        ' Instantiate the CancellationTokenSource.  
        cts = New CancellationTokenSource()  
  
        resultsTextBox.Clear()  
  
        Try  
            ' ***Set up the CancellationTokenSource to cancel after 2.5 seconds. (You   
            ' can adjust the time.)  
            cts.CancelAfter(2500)  
  
            Await AccessTheWebAsync(cts.Token)  
            resultsTextBox.Text &= vbCrLf & "Downloads complete."  
  
        Catch ex As OperationCanceledException  
            resultsTextBox.Text &= vbCrLf & "Downloads canceled." & vbCrLf  
  
        Catch ex As Exception  
            resultsTextBox.Text &= vbCrLf & "Downloads failed." & vbCrLf  
        End Try  
  
        ' Set the CancellationTokenSource to Nothing when the download is complete.  
        cts = Nothing  
    End Sub  
  
    ' You can still include a Cancel button if you want to.  
    Private Sub cancelButton_Click(sender As Object, e As RoutedEventArgs)  
  
        If cts IsNot Nothing Then  
            cts.Cancel()  
        End If  
    End Sub  
  
    ' Provide a parameter for the CancellationToken.  
    ' Change the return type to Task because the method has no return statement.  
    Async Function AccessTheWebAsync(ct As CancellationToken) As Task  
  
        Dim client As HttpClient = New HttpClient()  
  
        ' Call SetUpURLList to make a list of web addresses.  
        Dim urlList As List(Of String) = SetUpURLList()  
  
        ' Process each element in the list of web addresses.  
        For Each url In urlList  
            ' GetAsync returns a Task(Of HttpResponseMessage).   
            ' Argument ct carries the message if the Cancel button is chosen.   
            ' Note that the Cancel button can cancel all remaining downloads.  
            Dim response As HttpResponseMessage = Await client.GetAsync(url, ct)  
  
            ' Retrieve the website contents from the HttpResponseMessage.  
            Dim urlContents As Byte() = Await response.Content.ReadAsByteArrayAsync()  
  
            resultsTextBox.Text &=  
                String.Format(vbCrLf & "Length of the downloaded string: {0}." & vbCrLf, urlContents.Length)  
        Next  
    End Function  
  
    ' Add a method that creates a list of web addresses.  
    Private Function SetUpURLList() As List(Of String)  
  
        Dim urls = New List(Of String) From  
            {  
                "https://msdn.microsoft.com",  
                "https://msdn.microsoft.com/library/hh290138.aspx",  
                "https://msdn.microsoft.com/library/hh290140.aspx",  
                "https://msdn.microsoft.com/library/dd470362.aspx",  
                "https://msdn.microsoft.com/library/aa578028.aspx",  
                "https://msdn.microsoft.com/library/ms404677.aspx",  
                "https://msdn.microsoft.com/library/ff730837.aspx"  
            }  
        Return urls  
    End Function  
  
End Class  
  
' Sample output:  
  
' Length of the downloaded string: 35990.  
  
' Length of the downloaded string: 407399.  
  
' Length of the downloaded string: 226091.  
  
' Downloads canceled.  
```  
  
## <a name="see-also"></a>関連項目  
 [Async および Await を使用した非同期プログラミング (Visual Basic)](../../../../visual-basic/programming-guide/concepts/async/index.md)  
 [チュートリアル: Async と Await を使用した Web へのアクセス (Visual Basic)](../../../../visual-basic/programming-guide/concepts/async/walkthrough-accessing-the-web-by-using-async-and-await.md)  
 [非同期タスクまたはタスク (Visual Basic) の一覧をキャンセルします。](../../../../visual-basic/programming-guide/concepts/async/cancel-an-async-task-or-a-list-of-tasks.md)  
 [非同期アプリケーションの微調整 (Visual Basic)](../../../../visual-basic/programming-guide/concepts/async/fine-tuning-your-async-application.md)  
 [非同期のサンプル: アプリケーションの微調整](https://code.msdn.microsoft.com/Async-Fine-Tuning-Your-a676abea)
