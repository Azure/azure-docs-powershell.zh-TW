---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 19d8c4e3a47f7b75073d0207d000b8f18a5c0f6f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957637"
---
# <span data-ttu-id="3c4e7-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3c4e7-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="3c4e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c4e7-102">SYNOPSIS</span></span>
<span data-ttu-id="3c4e7-103">更新現有的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="3c4e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c4e7-104">SYNTAX</span></span>

### <span data-ttu-id="3c4e7-105">SpObjectIdWithDisplayNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3c4e7-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c4e7-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c4e7-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c4e7-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c4e7-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c4e7-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c4e7-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c4e7-109">說明</span><span class="sxs-lookup"><span data-stu-id="3c4e7-109">DESCRIPTION</span></span>
<span data-ttu-id="3c4e7-110">更新現有的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="3c4e7-111">若要更新與此服務主體相關聯的認證，請使用 New-AzADSpCredential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="3c4e7-112">若要更新與基礎應用程式相關聯的屬性，請使用 Update-AzADApplication Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="3c4e7-113">示例</span><span class="sxs-lookup"><span data-stu-id="3c4e7-113">EXAMPLES</span></span>

### <span data-ttu-id="3c4e7-114">範例 1-更新服務主體的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="3c4e7-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="3c4e7-115">將包含物件 id ' 784136ca-3ae2-4fdd-a388-89d793e7c780」的服務主體的顯示名稱更新為「MyNewDisplayName」。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="3c4e7-116">範例 2-使用管道更新服務主體的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="3c4e7-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="3c4e7-117">取得 784136ca-3ae2-4fdd-a388-89d793e7c780 Cmdlet 之物件識別碼為「」和 Update-AzADServicePrincipal 管道的服務主體，以將服務主體的顯示名稱更新為 "MyNewDisplayName"。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="3c4e7-118">參數</span><span class="sxs-lookup"><span data-stu-id="3c4e7-118">PARAMETERS</span></span>

### <span data-ttu-id="3c4e7-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3c4e7-119">-ApplicationId</span></span>
<span data-ttu-id="3c4e7-120">要更新的服務主體的 [應用程式識別碼]。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-120">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="3c4e7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c4e7-121">-DefaultProfile</span></span>
<span data-ttu-id="3c4e7-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c4e7-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3c4e7-123">-DisplayName</span></span>
<span data-ttu-id="3c4e7-124">服務主體的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-124">The display name for the service principal.</span></span>

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

### <span data-ttu-id="3c4e7-125">-首頁</span><span class="sxs-lookup"><span data-stu-id="3c4e7-125">-Homepage</span></span>
<span data-ttu-id="3c4e7-126">服務主體的首頁。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-126">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="3c4e7-127">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="3c4e7-127">-IdentifierUri</span></span>
<span data-ttu-id="3c4e7-128">服務主體的識別碼 URI (s) 。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-128">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="3c4e7-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c4e7-129">-InputObject</span></span>
<span data-ttu-id="3c4e7-130">代表要更新之服務主體的物件。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-130">The object representing the service principal to update.</span></span>

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

### <span data-ttu-id="3c4e7-131">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="3c4e7-131">-KeyCredential</span></span>
<span data-ttu-id="3c4e7-132">服務主體 (s) 的金鑰認證。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-132">The key credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="3c4e7-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3c4e7-133">-ObjectId</span></span>
<span data-ttu-id="3c4e7-134">要更新的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-134">The object id of the service principal to update.</span></span>

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

### <span data-ttu-id="3c4e7-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="3c4e7-135">-PasswordCredential</span></span>
<span data-ttu-id="3c4e7-136">服務主體的密碼認證 (s) 。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-136">The password credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="3c4e7-137">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3c4e7-137">-ServicePrincipalName</span></span>
<span data-ttu-id="3c4e7-138">要更新的服務主體的 SPN。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-138">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="3c4e7-139">-確認</span><span class="sxs-lookup"><span data-stu-id="3c4e7-139">-Confirm</span></span>
<span data-ttu-id="3c4e7-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c4e7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c4e7-141">-WhatIf</span></span>
<span data-ttu-id="3c4e7-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c4e7-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c4e7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c4e7-144">CommonParameters</span></span>
<span data-ttu-id="3c4e7-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c4e7-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c4e7-147">輸入</span><span class="sxs-lookup"><span data-stu-id="3c4e7-147">INPUTS</span></span>

### <span data-ttu-id="3c4e7-148">System.object</span><span class="sxs-lookup"><span data-stu-id="3c4e7-148">System.String</span></span>

### <span data-ttu-id="3c4e7-149">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="3c4e7-149">System.Guid</span></span>

### <span data-ttu-id="3c4e7-150">PSADServicePrincipal （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-150">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="3c4e7-151">輸出</span><span class="sxs-lookup"><span data-stu-id="3c4e7-151">OUTPUTS</span></span>

### <span data-ttu-id="3c4e7-152">PSADServicePrincipal （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="3c4e7-152">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="3c4e7-153">筆記</span><span class="sxs-lookup"><span data-stu-id="3c4e7-153">NOTES</span></span>

## <span data-ttu-id="3c4e7-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c4e7-154">RELATED LINKS</span></span>
