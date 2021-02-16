---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5312556cb49d02ea901b4cb2526a36f7237f66d1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404168"
---
# <span data-ttu-id="146e4-101">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="146e4-101">New-AzureSqlDatabaseServerContext</span></span>

## <span data-ttu-id="146e4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="146e4-102">SYNOPSIS</span></span>
<span data-ttu-id="146e4-103">建立伺服器連接上下文。</span><span class="sxs-lookup"><span data-stu-id="146e4-103">Creates a server connection context.</span></span>

## <span data-ttu-id="146e4-104">語法</span><span class="sxs-lookup"><span data-stu-id="146e4-104">SYNTAX</span></span>

### <span data-ttu-id="146e4-105">ByServerNameWithSqlAuth (預設) </span><span class="sxs-lookup"><span data-stu-id="146e4-105">ByServerNameWithSqlAuth (Default)</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="146e4-106">ByManageUrlWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="146e4-106">ByManageUrlWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="146e4-107">ByServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="146e4-107">ByServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="146e4-108">ByfullyQualifiedServerNameWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="146e4-108">ByFullyQualifiedServerNameWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="146e4-109">ByFullyQualifiedServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="146e4-109">ByFullyQualifiedServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="146e4-110">描述</span><span class="sxs-lookup"><span data-stu-id="146e4-110">DESCRIPTION</span></span>
<span data-ttu-id="146e4-111">**New-AzureSqlDatabaseServerCoNtext** Cmdlet 會建立 Azure SQL Database 伺服器連接上下文。</span><span class="sxs-lookup"><span data-stu-id="146e4-111">The **New-AzureSqlDatabaseServerContext** cmdlet creates an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="146e4-112">使用 SQL Server 驗證，使用指定的認證建立 SQL Database 伺服器的連接上下文。</span><span class="sxs-lookup"><span data-stu-id="146e4-112">Use SQL Server authentication to create a connection context to a SQL Database server by using the specified credentials.</span></span>
<span data-ttu-id="146e4-113">您可以根據名稱、完整名稱或 URL 來指定 SQL Database 伺服器。</span><span class="sxs-lookup"><span data-stu-id="146e4-113">You can specify the SQL Database server by name, by the fully qualified name, or by URL.</span></span>
<span data-ttu-id="146e4-114">若要取得認證，請使用Get-Credential指定使用者名稱和密碼的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="146e4-114">To obtain a credential, use the Get-Credential cmdlet that prompts you to specify the user name and password.</span></span>

<span data-ttu-id="146e4-115">使用 **New-AzureSqlDatabaseServerCoNtext** Cmdlet 與憑證式驗證，使用指定的 Azure 訂閱資料建立與指定的 SQL Database 伺服器之連結上下文。</span><span class="sxs-lookup"><span data-stu-id="146e4-115">Use the **New-AzureSqlDatabaseServerContext** cmdlet with certificate based authentication to create a connection context to the specified SQL Database server by using the specified Azure subscription data.</span></span>
<span data-ttu-id="146e4-116">您可以根據名稱或完整名稱指定 SQL Database 伺服器。</span><span class="sxs-lookup"><span data-stu-id="146e4-116">You can specify SQL Database server by name or by the fully qualified name.</span></span>
<span data-ttu-id="146e4-117">您可以將訂閱資料指定為參數，也可以從目前的 Azure 訂閱中取用。</span><span class="sxs-lookup"><span data-stu-id="146e4-117">You can specify the subscription data as a parameter or it can be retrieved from the current Azure subscription.</span></span>
<span data-ttu-id="146e4-118">使用 Select-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx Cmdlet 選取目前的 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="146e4-118">Use the Select-AzureSubscriptionhttps://msdn.microsoft.com/library/windowsazure/jj152833.aspx cmdlet to select the current Azure subscription.</span></span>

## <span data-ttu-id="146e4-119">例子</span><span class="sxs-lookup"><span data-stu-id="146e4-119">EXAMPLES</span></span>

### <span data-ttu-id="146e4-120">範例 1：使用 SQL Server 驗證建立上下文</span><span class="sxs-lookup"><span data-stu-id="146e4-120">Example 1: Create a context by using SQL Server authentication</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="146e4-121">此範例使用 SQL Server 驗證。</span><span class="sxs-lookup"><span data-stu-id="146e4-121">This example uses the SQL Server authentication.</span></span>

<span data-ttu-id="146e4-122">第一個命令會提示您輸入伺服器系統管理員認證，並且將認證儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="146e4-122">The first command prompts you for server administrator credentials, and stores the credentials in the $Credential variable.</span></span>

<span data-ttu-id="146e4-123">第二個命令會使用 $Credential 來連接到名為 lpqd0zbr8y 的 SQL Database $Credential。</span><span class="sxs-lookup"><span data-stu-id="146e4-123">The second command connects to the SQL Database server named lpqd0zbr8y by using $Credential.</span></span>

<span data-ttu-id="146e4-124">最後一個命令會在伺服器上建立名為 Database17 的資料庫，該資料庫是 $CoNtext。</span><span class="sxs-lookup"><span data-stu-id="146e4-124">The final command creates a database named Database17 on the server that is part of the context in $Context.</span></span>

### <span data-ttu-id="146e4-125">範例 2：使用憑證式驗證建立上下文</span><span class="sxs-lookup"><span data-stu-id="146e4-125">Example 2: Create a context by using certificate based authentication</span></span>
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

<span data-ttu-id="146e4-126">此範例使用憑證式驗證。</span><span class="sxs-lookup"><span data-stu-id="146e4-126">This example uses the certificate based authentication.</span></span>

<span data-ttu-id="146e4-127">前兩個命令會指派值給$SubscriptionId$Thumbprint變數。</span><span class="sxs-lookup"><span data-stu-id="146e4-127">The first two commands assign values to the $SubscriptionId and $Thumbprint variables.</span></span>

<span data-ttu-id="146e4-128">第三個命令會以指紋在 $Thumbprint 中識別憑證，並儲存在 $Certificate。</span><span class="sxs-lookup"><span data-stu-id="146e4-128">The third command gets the certificate identified by the thumbprint in $Thumbprint, and stores it in $Certificate.</span></span>

<span data-ttu-id="146e4-129">第四個命令將訂閱設定為 Subscription07，而第五個命令會選取該訂閱。</span><span class="sxs-lookup"><span data-stu-id="146e4-129">The fourth command sets the subscription to be Subscription07, and the fifth command selects that subscription.</span></span>

<span data-ttu-id="146e4-130">最後一個命令會針對名為 lpqd0zbr8y 的伺服器，于目前的訂閱中建立內容。</span><span class="sxs-lookup"><span data-stu-id="146e4-130">The final command creates a context in the current subscription for the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="146e4-131">參數</span><span class="sxs-lookup"><span data-stu-id="146e4-131">PARAMETERS</span></span>

### <span data-ttu-id="146e4-132">-認證</span><span class="sxs-lookup"><span data-stu-id="146e4-132">-Credential</span></span>
<span data-ttu-id="146e4-133">指定提供 SQL Server 驗證的認證物件，以存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="146e4-133">Specifies a credential object that provides SQL Server authentication for you to access the server.</span></span>

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

### <span data-ttu-id="146e4-134">-FullyQualifiedServerName</span><span class="sxs-lookup"><span data-stu-id="146e4-134">-FullyQualifiedServerName</span></span>
<span data-ttu-id="146e4-135">指定 Azure SQL Database 伺服器 (FQDN) 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="146e4-135">Specifies the fully qualified domain name (FQDN) name for the Azure SQL Database server.</span></span>
<span data-ttu-id="146e4-136">例如，Server02.database.windows.net。</span><span class="sxs-lookup"><span data-stu-id="146e4-136">For example, Server02.database.windows.net.</span></span>

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

### <span data-ttu-id="146e4-137">-ManageUrl</span><span class="sxs-lookup"><span data-stu-id="146e4-137">-ManageUrl</span></span>
<span data-ttu-id="146e4-138">指定此 Cmdlet 用來存取伺服器的 Azure SQL DatabaseManagement 入口網站的 URL。</span><span class="sxs-lookup"><span data-stu-id="146e4-138">Specifies the URL that this cmdlet uses to access the Azure SQL DatabaseManagement Portal for the server.</span></span>

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

### <span data-ttu-id="146e4-139">-設定檔</span><span class="sxs-lookup"><span data-stu-id="146e4-139">-Profile</span></span>
<span data-ttu-id="146e4-140">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="146e4-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="146e4-141">如果您未指定設定檔，此 Cmdlet 會從本地預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="146e4-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="146e4-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="146e4-142">-ServerName</span></span>
<span data-ttu-id="146e4-143">指定資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="146e4-143">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="146e4-144">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="146e4-144">-SubscriptionName</span></span>
<span data-ttu-id="146e4-145">指定此 Cmdlet 用來建立連接上下文的 Azure 訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="146e4-145">Specifies the name of the Azure subscription that this cmdlet uses to create the connection context.</span></span>
<span data-ttu-id="146e4-146">如果您沒有為此參數指定值，Cmdlet 會使用目前的訂閱。</span><span class="sxs-lookup"><span data-stu-id="146e4-146">If you do not specify a value for this parameter, the cmdlet uses the current subscription.</span></span>
<span data-ttu-id="146e4-147">執行 Select-AzureSubscription Cmdlet 以變更目前的訂閱。</span><span class="sxs-lookup"><span data-stu-id="146e4-147">Run the Select-AzureSubscription cmdlet to change the current subscription.</span></span>

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

### <span data-ttu-id="146e4-148">-UseSubscription</span><span class="sxs-lookup"><span data-stu-id="146e4-148">-UseSubscription</span></span>
<span data-ttu-id="146e4-149">表示此 Cmdlet 使用 Azure 訂閱建立連接上下文。</span><span class="sxs-lookup"><span data-stu-id="146e4-149">Indicates that this cmdlet uses Azure subscription for creating the connection context.</span></span>

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

### <span data-ttu-id="146e4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="146e4-150">CommonParameters</span></span>
<span data-ttu-id="146e4-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="146e4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="146e4-152">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="146e4-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="146e4-153">輸入</span><span class="sxs-lookup"><span data-stu-id="146e4-153">INPUTS</span></span>

## <span data-ttu-id="146e4-154">輸出</span><span class="sxs-lookup"><span data-stu-id="146e4-154">OUTPUTS</span></span>

### <span data-ttu-id="146e4-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceCoNtext</span><span class="sxs-lookup"><span data-stu-id="146e4-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span></span>

## <span data-ttu-id="146e4-156">筆記</span><span class="sxs-lookup"><span data-stu-id="146e4-156">NOTES</span></span>
* <span data-ttu-id="146e4-157">如果您驗證時沒有指定網域，而且如果您使用 Windows PowerShell 2.0，Get-Credential Cmdlet 會以使用者名稱為前 () 回反杠 () 例如 \\ \user。</span><span class="sxs-lookup"><span data-stu-id="146e4-157">If you authenticate without specifying a domain, and if you use Windows PowerShell 2.0, the Get-Credential cmdlet returns a backslash (\\) prepended to the username, for example, \user.</span></span> <span data-ttu-id="146e4-158">Windows PowerShell 3.0 不會新增反杠。</span><span class="sxs-lookup"><span data-stu-id="146e4-158">Windows PowerShell 3.0 does not add the backslash.</span></span> <span data-ttu-id="146e4-159">**New-AzureSqlDatabaseServerCoNtext** Cmdlet 的認證參數無法識別此反杠。 </span><span class="sxs-lookup"><span data-stu-id="146e4-159">This backslash is not recognized by the *Credential* parameter of the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span> <span data-ttu-id="146e4-160">若要移除它，請使用類似下列的命令：</span><span class="sxs-lookup"><span data-stu-id="146e4-160">To remove it, use commands similar to the following:</span></span>

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## <span data-ttu-id="146e4-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="146e4-161">RELATED LINKS</span></span>



[<span data-ttu-id="146e4-162">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="146e4-162">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="146e4-163">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="146e4-163">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="146e4-164">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="146e4-164">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="146e4-165">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="146e4-165">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


