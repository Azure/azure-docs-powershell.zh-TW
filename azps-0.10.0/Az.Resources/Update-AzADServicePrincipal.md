---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: e2c8e8fea9f8f86f06a9808158c50cb63915106b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795175"
---
# <span data-ttu-id="30086-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="30086-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="30086-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30086-102">SYNOPSIS</span></span>
<span data-ttu-id="30086-103">更新現有的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="30086-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="30086-104">句法</span><span class="sxs-lookup"><span data-stu-id="30086-104">SYNTAX</span></span>

### <span data-ttu-id="30086-105">SpObjectIdWithDisplayNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="30086-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <Guid> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30086-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="30086-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30086-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="30086-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30086-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="30086-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>]
 [-Homepage <String>] [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>]
 [-PasswordCredential <PasswordCredential[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30086-109">說明</span><span class="sxs-lookup"><span data-stu-id="30086-109">DESCRIPTION</span></span>
<span data-ttu-id="30086-110">更新現有的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="30086-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="30086-111">若要更新與此服務主體相關聯的認證，請使用 New-AzADSpCredential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30086-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="30086-112">若要更新與基礎應用程式相關聯的屬性，請使用 Update-AzADApplication Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30086-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="30086-113">示例</span><span class="sxs-lookup"><span data-stu-id="30086-113">EXAMPLES</span></span>

### <span data-ttu-id="30086-114">範例 1-更新服務主體的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="30086-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="30086-115">將包含物件 id ' 784136ca-3ae2-4fdd-a388-89d793e7c780」的服務主體的顯示名稱更新為「MyNewDisplayName」。</span><span class="sxs-lookup"><span data-stu-id="30086-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="30086-116">範例 2-使用管道更新服務主體的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="30086-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="30086-117">取得 784136ca-3ae2-4fdd-a388-89d793e7c780 Cmdlet 之物件識別碼為「」和 Update-AzADServicePrincipal 管道的服務主體，以將服務主體的顯示名稱更新為 "MyNewDisplayName"。</span><span class="sxs-lookup"><span data-stu-id="30086-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="30086-118">參數</span><span class="sxs-lookup"><span data-stu-id="30086-118">PARAMETERS</span></span>

### <span data-ttu-id="30086-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="30086-119">-ApplicationId</span></span>
<span data-ttu-id="30086-120">要更新的服務主體的 [應用程式識別碼]。</span><span class="sxs-lookup"><span data-stu-id="30086-120">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="30086-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30086-121">-DefaultProfile</span></span>
<span data-ttu-id="30086-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="30086-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30086-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="30086-123">-DisplayName</span></span>
<span data-ttu-id="30086-124">服務主體的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="30086-124">The display name for the service principal.</span></span>

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

### <span data-ttu-id="30086-125">-首頁</span><span class="sxs-lookup"><span data-stu-id="30086-125">-Homepage</span></span>
<span data-ttu-id="30086-126">服務主體的首頁。</span><span class="sxs-lookup"><span data-stu-id="30086-126">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="30086-127">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="30086-127">-IdentifierUri</span></span>
<span data-ttu-id="30086-128">服務主體的識別碼 URI (s) 。</span><span class="sxs-lookup"><span data-stu-id="30086-128">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="30086-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30086-129">-InputObject</span></span>
<span data-ttu-id="30086-130">代表要更新之服務主體的物件。</span><span class="sxs-lookup"><span data-stu-id="30086-130">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30086-131">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="30086-131">-KeyCredential</span></span>
<span data-ttu-id="30086-132">服務主體 (s) 的金鑰認證。</span><span class="sxs-lookup"><span data-stu-id="30086-132">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30086-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="30086-133">-ObjectId</span></span>
<span data-ttu-id="30086-134">要更新的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="30086-134">The object id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30086-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="30086-135">-PasswordCredential</span></span>
<span data-ttu-id="30086-136">服務主體的密碼認證 (s) 。</span><span class="sxs-lookup"><span data-stu-id="30086-136">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30086-137">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="30086-137">-ServicePrincipalName</span></span>
<span data-ttu-id="30086-138">要更新的服務主體的 SPN。</span><span class="sxs-lookup"><span data-stu-id="30086-138">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="30086-139">-確認</span><span class="sxs-lookup"><span data-stu-id="30086-139">-Confirm</span></span>
<span data-ttu-id="30086-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="30086-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30086-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30086-141">-WhatIf</span></span>
<span data-ttu-id="30086-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30086-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30086-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30086-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30086-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30086-144">CommonParameters</span></span>
<span data-ttu-id="30086-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30086-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30086-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="30086-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30086-147">輸入</span><span class="sxs-lookup"><span data-stu-id="30086-147">INPUTS</span></span>

### <span data-ttu-id="30086-148">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="30086-148">System.Guid</span></span>

### <span data-ttu-id="30086-149">System.object</span><span class="sxs-lookup"><span data-stu-id="30086-149">System.String</span></span>

### <span data-ttu-id="30086-150">Microsoft.Azure.Graph.RBAC.Version1_6 PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="30086-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="30086-151">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="30086-151">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="30086-152">輸出</span><span class="sxs-lookup"><span data-stu-id="30086-152">OUTPUTS</span></span>

### <span data-ttu-id="30086-153">Microsoft.Azure.Graph.RBAC.Version1_6 PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="30086-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="30086-154">筆記</span><span class="sxs-lookup"><span data-stu-id="30086-154">NOTES</span></span>

## <span data-ttu-id="30086-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="30086-155">RELATED LINKS</span></span>
