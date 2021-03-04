---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: beb51449ea0264defe640ba60ad687be405ab669
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904285"
---
# <span data-ttu-id="37117-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="37117-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="37117-102">簡介</span><span class="sxs-lookup"><span data-stu-id="37117-102">SYNOPSIS</span></span>
<span data-ttu-id="37117-103">為給定 SQL Server 實例新增透明資料加密憑證</span><span class="sxs-lookup"><span data-stu-id="37117-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="37117-104">語法</span><span class="sxs-lookup"><span data-stu-id="37117-104">SYNTAX</span></span>

### <span data-ttu-id="37117-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default) </span><span class="sxs-lookup"><span data-stu-id="37117-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37117-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37117-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37117-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37117-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37117-108">描述</span><span class="sxs-lookup"><span data-stu-id="37117-108">DESCRIPTION</span></span>
<span data-ttu-id="37117-109">此Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate為給定 SQL Server 實例新增透明資料加密憑證</span><span class="sxs-lookup"><span data-stu-id="37117-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="37117-110">例子</span><span class="sxs-lookup"><span data-stu-id="37117-110">EXAMPLES</span></span>

### <span data-ttu-id="37117-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="37117-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="37117-112">使用資源組名和 SQL Server 名稱將 TDE 憑證新增到 sql Server</span><span class="sxs-lookup"><span data-stu-id="37117-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="37117-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="37117-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="37117-114">使用伺服器 resourceId 將 TDE 憑證新增到伺服器</span><span class="sxs-lookup"><span data-stu-id="37117-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="37117-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="37117-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="37117-116">將 TDE 憑證新增到資源群組中所有的 sql 伺服器</span><span class="sxs-lookup"><span data-stu-id="37117-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="37117-117">參數</span><span class="sxs-lookup"><span data-stu-id="37117-117">PARAMETERS</span></span>

### <span data-ttu-id="37117-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37117-118">-DefaultProfile</span></span>
<span data-ttu-id="37117-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="37117-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37117-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37117-120">-PassThru</span></span>
<span data-ttu-id="37117-121">成功執行時，會返回已新增的憑證物件。</span><span class="sxs-lookup"><span data-stu-id="37117-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="37117-122">-密碼</span><span class="sxs-lookup"><span data-stu-id="37117-122">-Password</span></span>
<span data-ttu-id="37117-123">透明資料加密憑證的密碼</span><span class="sxs-lookup"><span data-stu-id="37117-123">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="37117-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="37117-124">-PrivateBlob</span></span>
<span data-ttu-id="37117-125">透明資料加密憑證的專用 Blob</span><span class="sxs-lookup"><span data-stu-id="37117-125">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="37117-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37117-126">-ResourceGroupName</span></span>
<span data-ttu-id="37117-127">資源組名</span><span class="sxs-lookup"><span data-stu-id="37117-127">The Resource Group Name</span></span>

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

### <span data-ttu-id="37117-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="37117-128">-ServerName</span></span>
<span data-ttu-id="37117-129">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="37117-129">The Server Name</span></span>

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

### <span data-ttu-id="37117-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="37117-130">-SqlServer</span></span>
<span data-ttu-id="37117-131">sql Server 輸入物件</span><span class="sxs-lookup"><span data-stu-id="37117-131">The sql server input object</span></span>

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

### <span data-ttu-id="37117-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="37117-132">-SqlServerResourceId</span></span>
<span data-ttu-id="37117-133">sql Server 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="37117-133">The sql server resource id</span></span>

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

### <span data-ttu-id="37117-134">-確認</span><span class="sxs-lookup"><span data-stu-id="37117-134">-Confirm</span></span>
<span data-ttu-id="37117-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="37117-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37117-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37117-136">-WhatIf</span></span>
<span data-ttu-id="37117-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="37117-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37117-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37117-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37117-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37117-139">CommonParameters</span></span>
<span data-ttu-id="37117-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="37117-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37117-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37117-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37117-142">輸入</span><span class="sxs-lookup"><span data-stu-id="37117-142">INPUTS</span></span>

### <span data-ttu-id="37117-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="37117-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="37117-144">System.String</span><span class="sxs-lookup"><span data-stu-id="37117-144">System.String</span></span>

## <span data-ttu-id="37117-145">輸出</span><span class="sxs-lookup"><span data-stu-id="37117-145">OUTPUTS</span></span>

### <span data-ttu-id="37117-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="37117-146">System.Boolean</span></span>

## <span data-ttu-id="37117-147">筆記</span><span class="sxs-lookup"><span data-stu-id="37117-147">NOTES</span></span>

## <span data-ttu-id="37117-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="37117-148">RELATED LINKS</span></span>
