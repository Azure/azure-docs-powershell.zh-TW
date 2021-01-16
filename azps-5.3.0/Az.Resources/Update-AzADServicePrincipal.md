---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 05bd5f7997c83c2be6b50faf0e6d88ee7413a773
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285940"
---
# <span data-ttu-id="323b2-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="323b2-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="323b2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="323b2-102">SYNOPSIS</span></span>
<span data-ttu-id="323b2-103">更新現有的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="323b2-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="323b2-104">句法</span><span class="sxs-lookup"><span data-stu-id="323b2-104">SYNTAX</span></span>

### <span data-ttu-id="323b2-105">SpObjectIdWithDisplayNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="323b2-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="323b2-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="323b2-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="323b2-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="323b2-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="323b2-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="323b2-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="323b2-109">說明</span><span class="sxs-lookup"><span data-stu-id="323b2-109">DESCRIPTION</span></span>
<span data-ttu-id="323b2-110">更新現有的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="323b2-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="323b2-111">若要更新與此服務主體相關聯的認證，請使用 New-AzADSpCredential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="323b2-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="323b2-112">若要更新與基礎應用程式相關聯的屬性，請使用 Update-AzADApplication Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="323b2-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="323b2-113">示例</span><span class="sxs-lookup"><span data-stu-id="323b2-113">EXAMPLES</span></span>

### <span data-ttu-id="323b2-114">範例1：更新服務主體的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="323b2-114">Example 1: Update the display name of a service principal</span></span>

```powershell
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="323b2-115">將包含物件 id ' 784136ca-3ae2-4fdd-a388-89d793e7c780」的服務主體的顯示名稱更新為「MyNewDisplayName」。</span><span class="sxs-lookup"><span data-stu-id="323b2-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="323b2-116">範例2：使用管道更新服務主體的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="323b2-116">Example 2: Update the display name of a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="323b2-117">取得 784136ca-3ae2-4fdd-a388-89d793e7c780 Cmdlet 之物件識別碼為「」和 Update-AzADServicePrincipal 管道的服務主體，以將服務主體的顯示名稱更新為 "MyNewDisplayName"。</span><span class="sxs-lookup"><span data-stu-id="323b2-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

### <span data-ttu-id="323b2-118">範例3</span><span class="sxs-lookup"><span data-stu-id="323b2-118">Example 3</span></span>

<span data-ttu-id="323b2-119">更新現有的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="323b2-119">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="323b2-120"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="323b2-120">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzADServicePrincipal -IdentifierUri https://mySecretApp1 -ObjectId 00000000-0000-0000-0000-00000000000000000
```

## <span data-ttu-id="323b2-121">參數</span><span class="sxs-lookup"><span data-stu-id="323b2-121">PARAMETERS</span></span>

### <span data-ttu-id="323b2-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="323b2-122">-ApplicationId</span></span>
<span data-ttu-id="323b2-123">要更新的服務主體的 [應用程式識別碼]。</span><span class="sxs-lookup"><span data-stu-id="323b2-123">The application id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpApplicationIdWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="323b2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="323b2-124">-DefaultProfile</span></span>
<span data-ttu-id="323b2-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="323b2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="323b2-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="323b2-126">-DisplayName</span></span>
<span data-ttu-id="323b2-127">服務主體的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="323b2-127">The display name for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet, SPNWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="323b2-128">-首頁</span><span class="sxs-lookup"><span data-stu-id="323b2-128">-Homepage</span></span>
<span data-ttu-id="323b2-129">服務主體的首頁。</span><span class="sxs-lookup"><span data-stu-id="323b2-129">The homepage for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="323b2-130">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="323b2-130">-IdentifierUri</span></span>
<span data-ttu-id="323b2-131">服務主體的識別碼 URI (s) 。</span><span class="sxs-lookup"><span data-stu-id="323b2-131">The identifier URI(s) for the service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="323b2-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="323b2-132">-InputObject</span></span>
<span data-ttu-id="323b2-133">代表要更新之服務主體的物件。</span><span class="sxs-lookup"><span data-stu-id="323b2-133">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="323b2-134">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="323b2-134">-KeyCredential</span></span>
<span data-ttu-id="323b2-135">服務主體 (s) 的金鑰認證。</span><span class="sxs-lookup"><span data-stu-id="323b2-135">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="323b2-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="323b2-136">-ObjectId</span></span>
<span data-ttu-id="323b2-137">要更新的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="323b2-137">The object id of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="323b2-138">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="323b2-138">-PasswordCredential</span></span>
<span data-ttu-id="323b2-139">服務主體的密碼認證 (s) 。</span><span class="sxs-lookup"><span data-stu-id="323b2-139">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="323b2-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="323b2-140">-ServicePrincipalName</span></span>
<span data-ttu-id="323b2-141">要更新的服務主體的 SPN。</span><span class="sxs-lookup"><span data-stu-id="323b2-141">The SPN of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="323b2-142">-確認</span><span class="sxs-lookup"><span data-stu-id="323b2-142">-Confirm</span></span>
<span data-ttu-id="323b2-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="323b2-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="323b2-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="323b2-144">-WhatIf</span></span>
<span data-ttu-id="323b2-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="323b2-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="323b2-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="323b2-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="323b2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="323b2-147">CommonParameters</span></span>
<span data-ttu-id="323b2-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="323b2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="323b2-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="323b2-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="323b2-150">輸入</span><span class="sxs-lookup"><span data-stu-id="323b2-150">INPUTS</span></span>

### <span data-ttu-id="323b2-151">System.object</span><span class="sxs-lookup"><span data-stu-id="323b2-151">System.String</span></span>

### <span data-ttu-id="323b2-152">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="323b2-152">System.Guid</span></span>

### <span data-ttu-id="323b2-153">PSADServicePrincipal （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="323b2-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="323b2-154">輸出</span><span class="sxs-lookup"><span data-stu-id="323b2-154">OUTPUTS</span></span>

### <span data-ttu-id="323b2-155">PSADServicePrincipal （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="323b2-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="323b2-156">筆記</span><span class="sxs-lookup"><span data-stu-id="323b2-156">NOTES</span></span>

## <span data-ttu-id="323b2-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="323b2-157">RELATED LINKS</span></span>