---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 73a124070dd329daff52ec5c0de16fb55ef74354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907314"
---
# <span data-ttu-id="dd8bb-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dd8bb-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="dd8bb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dd8bb-102">SYNOPSIS</span></span>
<span data-ttu-id="dd8bb-103">在管理群組中取得部署</span><span class="sxs-lookup"><span data-stu-id="dd8bb-103">Get deployment at a management group</span></span>

## <span data-ttu-id="dd8bb-104">語法</span><span class="sxs-lookup"><span data-stu-id="dd8bb-104">SYNTAX</span></span>

### <span data-ttu-id="dd8bb-105">GetByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="dd8bb-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd8bb-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="dd8bb-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd8bb-107">描述</span><span class="sxs-lookup"><span data-stu-id="dd8bb-107">DESCRIPTION</span></span>
<span data-ttu-id="dd8bb-108">**Get-AzManagementGroupDeployment** Cmdlet 會取得管理群組的部署。</span><span class="sxs-lookup"><span data-stu-id="dd8bb-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="dd8bb-109">指定 *名稱* 或 *Id* 參數以篩選結果。</span><span class="sxs-lookup"><span data-stu-id="dd8bb-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="dd8bb-110">根據預設 **，Get-AzManagementGroupDeployment 會** 取得管理群組的所有部署。</span><span class="sxs-lookup"><span data-stu-id="dd8bb-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="dd8bb-111">例子</span><span class="sxs-lookup"><span data-stu-id="dd8bb-111">EXAMPLES</span></span>

### <span data-ttu-id="dd8bb-112">範例 1：在管理群組中取得所有部署</span><span class="sxs-lookup"><span data-stu-id="dd8bb-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="dd8bb-113">此命令會獲得管理群組 「myMG」的所有部署。</span><span class="sxs-lookup"><span data-stu-id="dd8bb-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="dd8bb-114">範例 2：根據名稱取得部署</span><span class="sxs-lookup"><span data-stu-id="dd8bb-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="dd8bb-115">此命令在管理群組 「myMG」中會獲得「部署01」部署。</span><span class="sxs-lookup"><span data-stu-id="dd8bb-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="dd8bb-116">您可以使用 **New-AzManagementGroupDeployment** Cmdlet 為部署建立時指派名稱。</span><span class="sxs-lookup"><span data-stu-id="dd8bb-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="dd8bb-117">如果您沒有指派名稱，Cmdlet 會根據用來建立部署的範本提供預設名稱。</span><span class="sxs-lookup"><span data-stu-id="dd8bb-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="dd8bb-118">範例 3：以識別碼取得部署</span><span class="sxs-lookup"><span data-stu-id="dd8bb-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="dd8bb-119">此命令在管理群組 「myMG」中會獲得「部署01」部署。</span><span class="sxs-lookup"><span data-stu-id="dd8bb-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="dd8bb-120">參數</span><span class="sxs-lookup"><span data-stu-id="dd8bb-120">PARAMETERS</span></span>

### <span data-ttu-id="dd8bb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd8bb-121">-DefaultProfile</span></span>
<span data-ttu-id="dd8bb-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd8bb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd8bb-123">-Id</span><span class="sxs-lookup"><span data-stu-id="dd8bb-123">-Id</span></span>
<span data-ttu-id="dd8bb-124">部署之完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd8bb-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="dd8bb-125">範例：/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="dd8bb-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8bb-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="dd8bb-126">-ManagementGroupId</span></span>
<span data-ttu-id="dd8bb-127">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd8bb-127">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8bb-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd8bb-128">-Name</span></span>
<span data-ttu-id="dd8bb-129">部署名稱。</span><span class="sxs-lookup"><span data-stu-id="dd8bb-129">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8bb-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="dd8bb-130">-Pre</span></span>
<span data-ttu-id="dd8bb-131">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="dd8bb-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="dd8bb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd8bb-132">CommonParameters</span></span>
<span data-ttu-id="dd8bb-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dd8bb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd8bb-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd8bb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd8bb-135">輸入</span><span class="sxs-lookup"><span data-stu-id="dd8bb-135">INPUTS</span></span>

### <span data-ttu-id="dd8bb-136">沒有</span><span class="sxs-lookup"><span data-stu-id="dd8bb-136">None</span></span>

## <span data-ttu-id="dd8bb-137">輸出</span><span class="sxs-lookup"><span data-stu-id="dd8bb-137">OUTPUTS</span></span>

### <span data-ttu-id="dd8bb-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="dd8bb-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="dd8bb-139">筆記</span><span class="sxs-lookup"><span data-stu-id="dd8bb-139">NOTES</span></span>

## <span data-ttu-id="dd8bb-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd8bb-140">RELATED LINKS</span></span>
