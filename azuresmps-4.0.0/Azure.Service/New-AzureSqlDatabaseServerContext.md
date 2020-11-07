---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdcd4788e3eefdce858cb88c0bf1885353f8a673
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967416"
---
# <span data-ttu-id="25b79-101">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="25b79-101">New-AzureSqlDatabaseServerContext</span></span>

## <span data-ttu-id="25b79-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25b79-102">SYNOPSIS</span></span>
<span data-ttu-id="25b79-103">建立伺服器連接內容。</span><span class="sxs-lookup"><span data-stu-id="25b79-103">Creates a server connection context.</span></span>

## <span data-ttu-id="25b79-104">句法</span><span class="sxs-lookup"><span data-stu-id="25b79-104">SYNTAX</span></span>

### <span data-ttu-id="25b79-105">ByServerNameWithSqlAuth (預設) </span><span class="sxs-lookup"><span data-stu-id="25b79-105">ByServerNameWithSqlAuth (Default)</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="25b79-106">ByManageUrlWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="25b79-106">ByManageUrlWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="25b79-107">ByServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="25b79-107">ByServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="25b79-108">ByFullyQualifiedServerNameWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="25b79-108">ByFullyQualifiedServerNameWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="25b79-109">ByFullyQualifiedServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="25b79-109">ByFullyQualifiedServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="25b79-110">說明</span><span class="sxs-lookup"><span data-stu-id="25b79-110">DESCRIPTION</span></span>
<span data-ttu-id="25b79-111">**AzureSqlDatabaseServerCoNtext** Cmdlet 會建立 Azure SQL Database server 連接內容。</span><span class="sxs-lookup"><span data-stu-id="25b79-111">The **New-AzureSqlDatabaseServerContext** cmdlet creates an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="25b79-112">使用 [SQL Server 驗證]，透過指定的認證，建立 SQL 資料庫伺服器的線上內容。</span><span class="sxs-lookup"><span data-stu-id="25b79-112">Use SQL Server authentication to create a connection context to a SQL Database server by using the specified credentials.</span></span>
<span data-ttu-id="25b79-113">您可以依名稱、完全限定名稱或 URL 來指定 SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="25b79-113">You can specify the SQL Database server by name, by the fully qualified name, or by URL.</span></span>
<span data-ttu-id="25b79-114">若要取得認證，請使用 Get-Credential 的 Cmdlet，提示您指定使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="25b79-114">To obtain a credential, use the Get-Credential cmdlet that prompts you to specify the user name and password.</span></span>

<span data-ttu-id="25b79-115">使用 **新的 AzureSqlDatabaseServerCoNtext** Cmdlet 與憑證的驗證，以使用指定的 Azure 訂閱資料來建立指定 SQL 資料庫伺服器的線上內容。</span><span class="sxs-lookup"><span data-stu-id="25b79-115">Use the **New-AzureSqlDatabaseServerContext** cmdlet with certificate based authentication to create a connection context to the specified SQL Database server by using the specified Azure subscription data.</span></span>
<span data-ttu-id="25b79-116">您可以依名稱或完全限定的名稱來指定 SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="25b79-116">You can specify SQL Database server by name or by the fully qualified name.</span></span>
<span data-ttu-id="25b79-117">您可以指定訂閱資料做為參數，也可以從目前的 Azure 訂閱中進行檢索。</span><span class="sxs-lookup"><span data-stu-id="25b79-117">You can specify the subscription data as a parameter or it can be retrieved from the current Azure subscription.</span></span>
<span data-ttu-id="25b79-118">使用 AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx Cmdlet 選取目前的 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="25b79-118">Use the Select-AzureSubscriptionhttps://msdn.microsoft.com/library/windowsazure/jj152833.aspx cmdlet to select the current Azure subscription.</span></span>

## <span data-ttu-id="25b79-119">示例</span><span class="sxs-lookup"><span data-stu-id="25b79-119">EXAMPLES</span></span>

### <span data-ttu-id="25b79-120">範例1：使用 SQL Server 驗證建立內容</span><span class="sxs-lookup"><span data-stu-id="25b79-120">Example 1: Create a context by using SQL Server authentication</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="25b79-121">這個範例使用 SQL Server 驗證。</span><span class="sxs-lookup"><span data-stu-id="25b79-121">This example uses the SQL Server authentication.</span></span>

<span data-ttu-id="25b79-122">第一個命令會提示您輸入伺服器管理員認證，並將認證儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="25b79-122">The first command prompts you for server administrator credentials, and stores the credentials in the $Credential variable.</span></span>

<span data-ttu-id="25b79-123">第二個命令會使用 $Credential 連接到名為 lpqd0zbr8y 的 SQL 資料庫伺服器。</span><span class="sxs-lookup"><span data-stu-id="25b79-123">The second command connects to the SQL Database server named lpqd0zbr8y by using $Credential.</span></span>

<span data-ttu-id="25b79-124">最後一個命令會在伺服器上建立一個名為 Database17 的資料庫，該資料庫是 $CoNtext 中之內容的一部分。</span><span class="sxs-lookup"><span data-stu-id="25b79-124">The final command creates a database named Database17 on the server that is part of the context in $Context.</span></span>

### <span data-ttu-id="25b79-125">範例2：使用憑證的驗證建立內容</span><span class="sxs-lookup"><span data-stu-id="25b79-125">Example 2: Create a context by using certificate based authentication</span></span>
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

<span data-ttu-id="25b79-126">這個範例使用的是以憑證為基礎的驗證。</span><span class="sxs-lookup"><span data-stu-id="25b79-126">This example uses the certificate based authentication.</span></span>

<span data-ttu-id="25b79-127">前兩個命令會將值指派給 $SubscriptionId，並 $Thumbprint 變數。</span><span class="sxs-lookup"><span data-stu-id="25b79-127">The first two commands assign values to the $SubscriptionId and $Thumbprint variables.</span></span>

<span data-ttu-id="25b79-128">第三個命令會在 $Thumbprint 中取得指紋所識別的憑證，並將它儲存在 $Certificate 中。</span><span class="sxs-lookup"><span data-stu-id="25b79-128">The third command gets the certificate identified by the thumbprint in $Thumbprint, and stores it in $Certificate.</span></span>

<span data-ttu-id="25b79-129">第四個命令會將訂閱設定為 Subscription07，而第五個命令則會選取該訂閱。</span><span class="sxs-lookup"><span data-stu-id="25b79-129">The fourth command sets the subscription to be Subscription07, and the fifth command selects that subscription.</span></span>

<span data-ttu-id="25b79-130">最後一個命令會在目前訂閱中建立名為 lpqd0zbr8y 的伺服器的內容。</span><span class="sxs-lookup"><span data-stu-id="25b79-130">The final command creates a context in the current subscription for the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="25b79-131">參數</span><span class="sxs-lookup"><span data-stu-id="25b79-131">PARAMETERS</span></span>

### <span data-ttu-id="25b79-132">-認證</span><span class="sxs-lookup"><span data-stu-id="25b79-132">-Credential</span></span>
<span data-ttu-id="25b79-133">指定認證物件，為您提供用於存取伺服器的 SQL Server 驗證。</span><span class="sxs-lookup"><span data-stu-id="25b79-133">Specifies a credential object that provides SQL Server authentication for you to access the server.</span></span>

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b79-134">-FullyQualifiedServerName</span><span class="sxs-lookup"><span data-stu-id="25b79-134">-FullyQualifiedServerName</span></span>
<span data-ttu-id="25b79-135">指定 Azure SQL 資料庫伺服器 (FQDN) 名稱的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="25b79-135">Specifies the fully qualified domain name (FQDN) name for the Azure SQL Database server.</span></span>
<span data-ttu-id="25b79-136">例如，Server02.database.windows.net。</span><span class="sxs-lookup"><span data-stu-id="25b79-136">For example, Server02.database.windows.net.</span></span>

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b79-137">-ManageUrl</span><span class="sxs-lookup"><span data-stu-id="25b79-137">-ManageUrl</span></span>
<span data-ttu-id="25b79-138">指定此 Cmdlet 用來存取伺服器的 Azure SQL DatabaseManagement 入口網站的 URL。</span><span class="sxs-lookup"><span data-stu-id="25b79-138">Specifies the URL that this cmdlet uses to access the Azure SQL DatabaseManagement Portal for the server.</span></span>

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b79-139">-設定檔</span><span class="sxs-lookup"><span data-stu-id="25b79-139">-Profile</span></span>
<span data-ttu-id="25b79-140">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="25b79-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="25b79-141">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="25b79-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b79-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="25b79-142">-ServerName</span></span>
<span data-ttu-id="25b79-143">指定資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="25b79-143">Specifies the name of the database server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b79-144">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="25b79-144">-SubscriptionName</span></span>
<span data-ttu-id="25b79-145">指定此 Cmdlet 用來建立連接內容之 Azure 訂閱的名稱。</span><span class="sxs-lookup"><span data-stu-id="25b79-145">Specifies the name of the Azure subscription that this cmdlet uses to create the connection context.</span></span>
<span data-ttu-id="25b79-146">如果您沒有指定此參數的值，該 Cmdlet 會使用目前的訂閱。</span><span class="sxs-lookup"><span data-stu-id="25b79-146">If you do not specify a value for this parameter, the cmdlet uses the current subscription.</span></span>
<span data-ttu-id="25b79-147">執行 Select-AzureSubscription Cmdlet 來變更目前的訂閱。</span><span class="sxs-lookup"><span data-stu-id="25b79-147">Run the Select-AzureSubscription cmdlet to change the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b79-148">-UseSubscription</span><span class="sxs-lookup"><span data-stu-id="25b79-148">-UseSubscription</span></span>
<span data-ttu-id="25b79-149">表示此 Cmdlet 使用 Azure 訂閱建立線上內容。</span><span class="sxs-lookup"><span data-stu-id="25b79-149">Indicates that this cmdlet uses Azure subscription for creating the connection context.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b79-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b79-150">CommonParameters</span></span>
<span data-ttu-id="25b79-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25b79-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b79-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="25b79-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b79-153">輸入</span><span class="sxs-lookup"><span data-stu-id="25b79-153">INPUTS</span></span>

## <span data-ttu-id="25b79-154">輸出</span><span class="sxs-lookup"><span data-stu-id="25b79-154">OUTPUTS</span></span>

### <span data-ttu-id="25b79-155">SqlDatabase. IServerDataServiceCoNtext （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="25b79-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span></span>

## <span data-ttu-id="25b79-156">筆記</span><span class="sxs-lookup"><span data-stu-id="25b79-156">NOTES</span></span>
* <span data-ttu-id="25b79-157">如果您在未指定網域的情況下進行驗證，而您使用的是 Windows PowerShell 2.0，則 Get-Credential Cmdlet 會傳回 () 前的反斜線 \\ ，例如 \user。</span><span class="sxs-lookup"><span data-stu-id="25b79-157">If you authenticate without specifying a domain, and if you use Windows PowerShell 2.0, the Get-Credential cmdlet returns a backslash (\\) prepended to the username, for example, \user.</span></span> <span data-ttu-id="25b79-158">Windows PowerShell 3.0 不會加上反斜線。</span><span class="sxs-lookup"><span data-stu-id="25b79-158">Windows PowerShell 3.0 does not add the backslash.</span></span> <span data-ttu-id="25b79-159">**AzureSqlDatabaseServerCoNtext** Cmdlet 的 *Credential* 參數無法辨識此反斜線。</span><span class="sxs-lookup"><span data-stu-id="25b79-159">This backslash is not recognized by the *Credential* parameter of the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span> <span data-ttu-id="25b79-160">若要移除它，請使用類似下列的命令：</span><span class="sxs-lookup"><span data-stu-id="25b79-160">To remove it, use commands similar to the following:</span></span>

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## <span data-ttu-id="25b79-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="25b79-161">RELATED LINKS</span></span>

[<span data-ttu-id="25b79-162">Azure SQL 資料庫 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="25b79-162">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="25b79-163">AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="25b79-163">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="25b79-164">新-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="25b79-164">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="25b79-165">移除-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="25b79-165">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="25b79-166">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="25b79-166">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


