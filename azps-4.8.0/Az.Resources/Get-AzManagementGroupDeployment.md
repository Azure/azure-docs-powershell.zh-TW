---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 79eeb4e1725adf38b2f1dc70fe181280312fa1e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135673"
---
# <span data-ttu-id="0d1f1-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0d1f1-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="0d1f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d1f1-102">SYNOPSIS</span></span>
<span data-ttu-id="0d1f1-103">在管理群組中取得部署</span><span class="sxs-lookup"><span data-stu-id="0d1f1-103">Get deployment at a management group</span></span>

## <span data-ttu-id="0d1f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d1f1-104">SYNTAX</span></span>

### <span data-ttu-id="0d1f1-105">GetByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="0d1f1-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d1f1-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="0d1f1-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d1f1-107">說明</span><span class="sxs-lookup"><span data-stu-id="0d1f1-107">DESCRIPTION</span></span>
<span data-ttu-id="0d1f1-108">**AzManagementGroupDeployment** Cmdlet 會取得管理群組的部署。</span><span class="sxs-lookup"><span data-stu-id="0d1f1-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="0d1f1-109">指定 *Name* 或 *Id* 參數來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="0d1f1-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="0d1f1-110">根據預設， **AzManagementGroupDeployment 會取得** 管理群組上的所有部署。</span><span class="sxs-lookup"><span data-stu-id="0d1f1-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="0d1f1-111">示例</span><span class="sxs-lookup"><span data-stu-id="0d1f1-111">EXAMPLES</span></span>

### <span data-ttu-id="0d1f1-112">範例1：取得管理群組的所有部署</span><span class="sxs-lookup"><span data-stu-id="0d1f1-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="0d1f1-113">這個命令會取得管理群組「myMG」的所有部署。</span><span class="sxs-lookup"><span data-stu-id="0d1f1-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="0d1f1-114">範例2：依名稱取得部署</span><span class="sxs-lookup"><span data-stu-id="0d1f1-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="0d1f1-115">這個命令會取得管理群組「myMG」的「Deploy01」部署。</span><span class="sxs-lookup"><span data-stu-id="0d1f1-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="0d1f1-116">您可以在使用 **新的 AzManagementGroupDeployment** Cmdlet 建立部署時，將名稱指派給部署。</span><span class="sxs-lookup"><span data-stu-id="0d1f1-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="0d1f1-117">如果您沒有指派名稱，則 Cmdlet 會根據用來建立部署的範本，提供預設名稱。</span><span class="sxs-lookup"><span data-stu-id="0d1f1-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="0d1f1-118">範例3：依識別碼取得部署</span><span class="sxs-lookup"><span data-stu-id="0d1f1-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="0d1f1-119">這個命令會取得管理群組「myMG」的「Deploy01」部署。</span><span class="sxs-lookup"><span data-stu-id="0d1f1-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="0d1f1-120">參數</span><span class="sxs-lookup"><span data-stu-id="0d1f1-120">PARAMETERS</span></span>

### <span data-ttu-id="0d1f1-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0d1f1-121">-ApiVersion</span></span>
<span data-ttu-id="0d1f1-122">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="0d1f1-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="0d1f1-123">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="0d1f1-123">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1f1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d1f1-124">-DefaultProfile</span></span>
<span data-ttu-id="0d1f1-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d1f1-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1f1-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="0d1f1-126">-Id</span></span>
<span data-ttu-id="0d1f1-127">部署的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d1f1-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="0d1f1-128">範例：/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="0d1f1-128">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1f1-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="0d1f1-129">-ManagementGroupId</span></span>
<span data-ttu-id="0d1f1-130">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d1f1-130">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1f1-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d1f1-131">-Name</span></span>
<span data-ttu-id="0d1f1-132">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d1f1-132">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1f1-133">-預先</span><span class="sxs-lookup"><span data-stu-id="0d1f1-133">-Pre</span></span>
<span data-ttu-id="0d1f1-134">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="0d1f1-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1f1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d1f1-135">CommonParameters</span></span>
<span data-ttu-id="0d1f1-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d1f1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d1f1-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0d1f1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d1f1-138">輸入</span><span class="sxs-lookup"><span data-stu-id="0d1f1-138">INPUTS</span></span>

### <span data-ttu-id="0d1f1-139">所有</span><span class="sxs-lookup"><span data-stu-id="0d1f1-139">None</span></span>

## <span data-ttu-id="0d1f1-140">輸出</span><span class="sxs-lookup"><span data-stu-id="0d1f1-140">OUTPUTS</span></span>

### <span data-ttu-id="0d1f1-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="0d1f1-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0d1f1-142">筆記</span><span class="sxs-lookup"><span data-stu-id="0d1f1-142">NOTES</span></span>

## <span data-ttu-id="0d1f1-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d1f1-143">RELATED LINKS</span></span>
