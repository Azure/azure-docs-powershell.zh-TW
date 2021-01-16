---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e90dac7c55c6edca849c483ccb21d4f37197883a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277544"
---
# <span data-ttu-id="ad93f-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="ad93f-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="ad93f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad93f-102">SYNOPSIS</span></span>
<span data-ttu-id="ad93f-103">針對指定的 SQL Server 實例新增透明的資料加密憑證</span><span class="sxs-lookup"><span data-stu-id="ad93f-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="ad93f-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad93f-104">SYNTAX</span></span>

### <span data-ttu-id="ad93f-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ad93f-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad93f-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad93f-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad93f-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad93f-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad93f-108">說明</span><span class="sxs-lookup"><span data-stu-id="ad93f-108">DESCRIPTION</span></span>
<span data-ttu-id="ad93f-109">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate 為指定的 SQL Server 實例新增透明的資料加密憑證</span><span class="sxs-lookup"><span data-stu-id="ad93f-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="ad93f-110">示例</span><span class="sxs-lookup"><span data-stu-id="ad93f-110">EXAMPLES</span></span>

### <span data-ttu-id="ad93f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ad93f-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="ad93f-112">使用資源組名稱和 SQL Server 名稱將 TDE 憑證新增至 sql server</span><span class="sxs-lookup"><span data-stu-id="ad93f-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="ad93f-113">範例2</span><span class="sxs-lookup"><span data-stu-id="ad93f-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="ad93f-114">使用伺服器 resourceId 將 TDE 憑證新增到伺服器</span><span class="sxs-lookup"><span data-stu-id="ad93f-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="ad93f-115">範例3</span><span class="sxs-lookup"><span data-stu-id="ad93f-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="ad93f-116">新增 TDE 憑證至資源群組中的所有 sql 伺服器</span><span class="sxs-lookup"><span data-stu-id="ad93f-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="ad93f-117">參數</span><span class="sxs-lookup"><span data-stu-id="ad93f-117">PARAMETERS</span></span>

### <span data-ttu-id="ad93f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad93f-118">-DefaultProfile</span></span>
<span data-ttu-id="ad93f-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad93f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad93f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad93f-120">-PassThru</span></span>
<span data-ttu-id="ad93f-121">成功執行時，會傳回已新增的憑證物件。</span><span class="sxs-lookup"><span data-stu-id="ad93f-121">On Successful execution, returns certificate object that was added.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad93f-122">-Password</span><span class="sxs-lookup"><span data-stu-id="ad93f-122">-Password</span></span>
<span data-ttu-id="ad93f-123">透明資料加密憑證的密碼</span><span class="sxs-lookup"><span data-stu-id="ad93f-123">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad93f-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="ad93f-124">-PrivateBlob</span></span>
<span data-ttu-id="ad93f-125">透明資料加密憑證的專用 blob</span><span class="sxs-lookup"><span data-stu-id="ad93f-125">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad93f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad93f-126">-ResourceGroupName</span></span>
<span data-ttu-id="ad93f-127">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="ad93f-127">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad93f-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ad93f-128">-ServerName</span></span>
<span data-ttu-id="ad93f-129">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="ad93f-129">The Server Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad93f-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="ad93f-130">-SqlServer</span></span>
<span data-ttu-id="ad93f-131">Sql server 輸入物件</span><span class="sxs-lookup"><span data-stu-id="ad93f-131">The sql server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad93f-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="ad93f-132">-SqlServerResourceId</span></span>
<span data-ttu-id="ad93f-133">Sql server 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ad93f-133">The sql server resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad93f-134">-確認</span><span class="sxs-lookup"><span data-stu-id="ad93f-134">-Confirm</span></span>
<span data-ttu-id="ad93f-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ad93f-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad93f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad93f-136">-WhatIf</span></span>
<span data-ttu-id="ad93f-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ad93f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad93f-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad93f-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad93f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad93f-139">CommonParameters</span></span>
<span data-ttu-id="ad93f-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad93f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad93f-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ad93f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad93f-142">輸入</span><span class="sxs-lookup"><span data-stu-id="ad93f-142">INPUTS</span></span>

### <span data-ttu-id="ad93f-143">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="ad93f-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="ad93f-144">System.object</span><span class="sxs-lookup"><span data-stu-id="ad93f-144">System.String</span></span>

## <span data-ttu-id="ad93f-145">輸出</span><span class="sxs-lookup"><span data-stu-id="ad93f-145">OUTPUTS</span></span>

### <span data-ttu-id="ad93f-146">System.object</span><span class="sxs-lookup"><span data-stu-id="ad93f-146">System.Boolean</span></span>

## <span data-ttu-id="ad93f-147">筆記</span><span class="sxs-lookup"><span data-stu-id="ad93f-147">NOTES</span></span>

## <span data-ttu-id="ad93f-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad93f-148">RELATED LINKS</span></span>
