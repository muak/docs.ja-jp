### <a name="improved-wcf-chain-trust-certificate-validation-for-nettcp-certificate-authentication"></a><span data-ttu-id="52e6d-101">Net.Tcp 証明書認証の WCF チェーン信頼証明書の検証が向上した</span><span class="sxs-lookup"><span data-stu-id="52e6d-101">Improved WCF chain trust certificate validation for Net.Tcp certificate authentication</span></span>

|   |   |
|---|---|
|<span data-ttu-id="52e6d-102">説明</span><span class="sxs-lookup"><span data-stu-id="52e6d-102">Details</span></span>|<span data-ttu-id="52e6d-103">.NET Framework 4.7.2 では、WCF とのトランスポート セキュリティで証明書認証を使用するときのチェーン信頼証明書の検証が向上しています。</span><span class="sxs-lookup"><span data-stu-id="52e6d-103">.NET Framework 4.7.2 improves chain trust certificate validation when using certificate authentication with transport security with WCF.</span></span> <span data-ttu-id="52e6d-104">この改善により、サーバーに対する認証に使用されるクライアント証明書を、クライアント認証用に構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52e6d-104">With this improvement, client certificates that are used to authenticate to a server must be configured for client authentication.</span></span>  <span data-ttu-id="52e6d-105">同様に、サーバーを認証するためのサーバー証明書は、サーバー認証用に構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52e6d-105">Similarly server certificates that are for the authenticating a server must be configured for server authentication.</span></span> <span data-ttu-id="52e6d-106">この変更では、ルート証明書が無効になっている場合、証明書チェーンの検証が失敗します。</span><span class="sxs-lookup"><span data-stu-id="52e6d-106">With this change, if the root certificate is disabled, the certificate chain validation fails.</span></span> <span data-ttu-id="52e6d-107">同じ変更が、Windows セキュリティ ロールアップによって .NET Framework 3.5 以降のバージョンにも行われました。</span><span class="sxs-lookup"><span data-stu-id="52e6d-107">The same change was also made to .NET Framework 3.5 and later versions via Windows security roll-up.</span></span> <span data-ttu-id="52e6d-108">詳細については、[こちら](https://support.microsoft.com/en-us/help/4055269/security-only-update-for-net-framework-3-5-1-4-5-2-4-6-4-6-1-4-6-2-4-7)をご覧ください。この変更は既定で有効になり、構成設定によって無効にできます。</span><span class="sxs-lookup"><span data-stu-id="52e6d-108">You can find more information [here](https://support.microsoft.com/en-us/help/4055269/security-only-update-for-net-framework-3-5-1-4-5-2-4-6-4-6-1-4-6-2-4-7).This change is on by default and can be turned off by a configuration setting.</span></span>|
|<span data-ttu-id="52e6d-109">提案される解決策</span><span class="sxs-lookup"><span data-stu-id="52e6d-109">Suggestion</span></span>|<ul><li><span data-ttu-id="52e6d-110">サーバー証明書とクライアント証明書に必要な EKU OID があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="52e6d-110">Validate if your server and client certification has the required EKU OID.</span></span> <span data-ttu-id="52e6d-111">ない場合は、証明書を更新します。</span><span class="sxs-lookup"><span data-stu-id="52e6d-111">If not, update your certification.</span></span></li><li><span data-ttu-id="52e6d-112">ルート証明書が無効かどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="52e6d-112">Validate if your root certificate is invalid.</span></span> <span data-ttu-id="52e6d-113">無効である場合は、ルート証明書を更新します。</span><span class="sxs-lookup"><span data-stu-id="52e6d-113">If so, update the root certificate.</span></span></li><li><span data-ttu-id="52e6d-114">変更をオプトアウトする方法: 証明書を更新できない場合は、次の構成設定により互換性に影響する変更を一時的に回避できます。ただし、変更をオプトアウトすると、システムはセキュリティの問題に対して脆弱なままになります。</span><span class="sxs-lookup"><span data-stu-id="52e6d-114">How to opt out of the change: If you can't update the certificate, you can work around the breaking change temporarily with the following configration setting,  However, opting out of the change will leave your system vulnerable to the security issue.</span></span></li></ul><pre><code class="lang-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;wcf:useLegacyCertificateUsagePolicy&quot; value=&quot;true&quot; /&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="52e6d-115">スコープ</span><span class="sxs-lookup"><span data-stu-id="52e6d-115">Scope</span></span>|<span data-ttu-id="52e6d-116">マイナー</span><span class="sxs-lookup"><span data-stu-id="52e6d-116">Minor</span></span>|
|<span data-ttu-id="52e6d-117">Version</span><span class="sxs-lookup"><span data-stu-id="52e6d-117">Version</span></span>|<span data-ttu-id="52e6d-118">4.7.2</span><span class="sxs-lookup"><span data-stu-id="52e6d-118">4.7.2</span></span>|
|<span data-ttu-id="52e6d-119">型</span><span class="sxs-lookup"><span data-stu-id="52e6d-119">Type</span></span>|<span data-ttu-id="52e6d-120">ランタイム</span><span class="sxs-lookup"><span data-stu-id="52e6d-120">Runtime</span></span>|
