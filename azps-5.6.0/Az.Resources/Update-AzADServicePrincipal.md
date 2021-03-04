---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 44091f612720851a0ab13d54716f441d73a04065
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914402"
---
# <span data-ttu-id="50fde-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="50fde-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="50fde-102">簡介</span><span class="sxs-lookup"><span data-stu-id="50fde-102">SYNOPSIS</span></span>
<span data-ttu-id="50fde-103">更新現有的 Azure Active Directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="50fde-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="50fde-104">語法</span><span class="sxs-lookup"><span data-stu-id="50fde-104">SYNTAX</span></span>

### <span data-ttu-id="50fde-105">SpObjectIdWithDisplayNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="50fde-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50fde-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="50fde-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50fde-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="50fde-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50fde-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="50fde-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50fde-109">描述</span><span class="sxs-lookup"><span data-stu-id="50fde-109">DESCRIPTION</span></span>
<span data-ttu-id="50fde-110">更新現有的 Azure Active Directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="50fde-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="50fde-111">若要更新與此服務主體相關聯的認證，請使用 New-AzADSpCredential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50fde-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="50fde-112">若要更新與基礎應用程式關聯的屬性，請使用 Update-AzADApplication Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50fde-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="50fde-113">例子</span><span class="sxs-lookup"><span data-stu-id="50fde-113">EXAMPLES</span></span>

### <span data-ttu-id="50fde-114">範例 1：更新服務主體的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="50fde-114">Example 1: Update the display name of a service principal</span></span>

```powershell
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="50fde-115">將服務主體的顯示名稱與物件識別碼 '784136ca-3ae2-4fdd-a388-89d793e7c780' 更新為 'MyNewDisplayName'。</span><span class="sxs-lookup"><span data-stu-id="50fde-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="50fde-116">範例 2：使用管線更新服務主體的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="50fde-116">Example 2: Update the display name of a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="50fde-117">使用物件識別碼 '784136ca-3ae2-4fdd-a388-89d793e7c780' 和服務主體管道到 Update-AzADServicePrincipal Cmdlet，將服務主體的顯示名稱更新為 「MyNewDisplayName」的服務主體。</span><span class="sxs-lookup"><span data-stu-id="50fde-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

### <span data-ttu-id="50fde-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="50fde-118">Example 3</span></span>

<span data-ttu-id="50fde-119">更新現有的 Azure Active Directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="50fde-119">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="50fde-120"> (自動) </span><span class="sxs-lookup"><span data-stu-id="50fde-120">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzADServicePrincipal -IdentifierUri https://mySecretApp1 -ObjectId 00000000-0000-0000-0000-00000000000000000
```

## <span data-ttu-id="50fde-121">參數</span><span class="sxs-lookup"><span data-stu-id="50fde-121">PARAMETERS</span></span>

### <span data-ttu-id="50fde-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="50fde-122">-ApplicationId</span></span>
<span data-ttu-id="50fde-123">要更新的服務主體之應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="50fde-123">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="50fde-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50fde-124">-DefaultProfile</span></span>
<span data-ttu-id="50fde-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="50fde-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50fde-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="50fde-126">-DisplayName</span></span>
<span data-ttu-id="50fde-127">服務主體的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="50fde-127">The display name for the service principal.</span></span>

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

### <span data-ttu-id="50fde-128">-首頁</span><span class="sxs-lookup"><span data-stu-id="50fde-128">-Homepage</span></span>
<span data-ttu-id="50fde-129">服務主體的首頁。</span><span class="sxs-lookup"><span data-stu-id="50fde-129">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="50fde-130">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="50fde-130">-IdentifierUri</span></span>
<span data-ttu-id="50fde-131">識別碼 URI 會 () 主體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="50fde-131">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="50fde-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50fde-132">-InputObject</span></span>
<span data-ttu-id="50fde-133">代表要更新之服務主體的物件。</span><span class="sxs-lookup"><span data-stu-id="50fde-133">The object representing the service principal to update.</span></span>

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

### <span data-ttu-id="50fde-134">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="50fde-134">-KeyCredential</span></span>
<span data-ttu-id="50fde-135">金鑰認證 () 主體的認證。</span><span class="sxs-lookup"><span data-stu-id="50fde-135">The key credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="50fde-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="50fde-136">-ObjectId</span></span>
<span data-ttu-id="50fde-137">要更新的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="50fde-137">The object id of the service principal to update.</span></span>

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

### <span data-ttu-id="50fde-138">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="50fde-138">-PasswordCredential</span></span>
<span data-ttu-id="50fde-139">密碼認證 () 主體的認證。</span><span class="sxs-lookup"><span data-stu-id="50fde-139">The password credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="50fde-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="50fde-140">-ServicePrincipalName</span></span>
<span data-ttu-id="50fde-141">要更新的服務主體 SPN。</span><span class="sxs-lookup"><span data-stu-id="50fde-141">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="50fde-142">-確認</span><span class="sxs-lookup"><span data-stu-id="50fde-142">-Confirm</span></span>
<span data-ttu-id="50fde-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="50fde-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50fde-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50fde-144">-WhatIf</span></span>
<span data-ttu-id="50fde-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50fde-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50fde-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50fde-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50fde-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50fde-147">CommonParameters</span></span>
<span data-ttu-id="50fde-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="50fde-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50fde-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50fde-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50fde-150">輸入</span><span class="sxs-lookup"><span data-stu-id="50fde-150">INPUTS</span></span>

### <span data-ttu-id="50fde-151">System.String</span><span class="sxs-lookup"><span data-stu-id="50fde-151">System.String</span></span>

### <span data-ttu-id="50fde-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="50fde-152">System.Guid</span></span>

### <span data-ttu-id="50fde-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="50fde-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="50fde-154">輸出</span><span class="sxs-lookup"><span data-stu-id="50fde-154">OUTPUTS</span></span>

### <span data-ttu-id="50fde-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="50fde-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="50fde-156">筆記</span><span class="sxs-lookup"><span data-stu-id="50fde-156">NOTES</span></span>

## <span data-ttu-id="50fde-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="50fde-157">RELATED LINKS</span></span>