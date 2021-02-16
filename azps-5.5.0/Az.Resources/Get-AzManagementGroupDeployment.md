---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 6c873dfda563c24104abc5e89b00569358084d96
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141859"
---
# <span data-ttu-id="646e6-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="646e6-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="646e6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="646e6-102">SYNOPSIS</span></span>
<span data-ttu-id="646e6-103">在管理群組中取得部署</span><span class="sxs-lookup"><span data-stu-id="646e6-103">Get deployment at a management group</span></span>

## <span data-ttu-id="646e6-104">句法</span><span class="sxs-lookup"><span data-stu-id="646e6-104">SYNTAX</span></span>

### <span data-ttu-id="646e6-105">GetByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="646e6-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="646e6-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="646e6-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="646e6-107">說明</span><span class="sxs-lookup"><span data-stu-id="646e6-107">DESCRIPTION</span></span>
<span data-ttu-id="646e6-108">**AzManagementGroupDeployment** Cmdlet 會取得管理群組的部署。</span><span class="sxs-lookup"><span data-stu-id="646e6-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="646e6-109">指定 *Name* 或 *Id* 參數來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="646e6-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="646e6-110">根據預設， **AzManagementGroupDeployment 會取得** 管理群組上的所有部署。</span><span class="sxs-lookup"><span data-stu-id="646e6-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="646e6-111">示例</span><span class="sxs-lookup"><span data-stu-id="646e6-111">EXAMPLES</span></span>

### <span data-ttu-id="646e6-112">範例1：取得管理群組的所有部署</span><span class="sxs-lookup"><span data-stu-id="646e6-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="646e6-113">這個命令會取得管理群組「myMG」的所有部署。</span><span class="sxs-lookup"><span data-stu-id="646e6-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="646e6-114">範例2：依名稱取得部署</span><span class="sxs-lookup"><span data-stu-id="646e6-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="646e6-115">這個命令會取得管理群組「myMG」的「Deploy01」部署。</span><span class="sxs-lookup"><span data-stu-id="646e6-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="646e6-116">您可以在使用 **新的 AzManagementGroupDeployment** Cmdlet 建立部署時，將名稱指派給部署。</span><span class="sxs-lookup"><span data-stu-id="646e6-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="646e6-117">如果您沒有指派名稱，則 Cmdlet 會根據用來建立部署的範本，提供預設名稱。</span><span class="sxs-lookup"><span data-stu-id="646e6-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="646e6-118">範例3：依識別碼取得部署</span><span class="sxs-lookup"><span data-stu-id="646e6-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="646e6-119">這個命令會取得管理群組「myMG」的「Deploy01」部署。</span><span class="sxs-lookup"><span data-stu-id="646e6-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="646e6-120">參數</span><span class="sxs-lookup"><span data-stu-id="646e6-120">PARAMETERS</span></span>

### <span data-ttu-id="646e6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="646e6-121">-DefaultProfile</span></span>
<span data-ttu-id="646e6-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="646e6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="646e6-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="646e6-123">-Id</span></span>
<span data-ttu-id="646e6-124">部署的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="646e6-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="646e6-125">範例：/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="646e6-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="646e6-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="646e6-126">-ManagementGroupId</span></span>
<span data-ttu-id="646e6-127">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="646e6-127">The management group id.</span></span>

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

### <span data-ttu-id="646e6-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="646e6-128">-Name</span></span>
<span data-ttu-id="646e6-129">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="646e6-129">The name of deployment.</span></span>

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

### <span data-ttu-id="646e6-130">-預先</span><span class="sxs-lookup"><span data-stu-id="646e6-130">-Pre</span></span>
<span data-ttu-id="646e6-131">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="646e6-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="646e6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="646e6-132">CommonParameters</span></span>
<span data-ttu-id="646e6-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="646e6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="646e6-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="646e6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="646e6-135">輸入</span><span class="sxs-lookup"><span data-stu-id="646e6-135">INPUTS</span></span>

### <span data-ttu-id="646e6-136">所有</span><span class="sxs-lookup"><span data-stu-id="646e6-136">None</span></span>

## <span data-ttu-id="646e6-137">輸出</span><span class="sxs-lookup"><span data-stu-id="646e6-137">OUTPUTS</span></span>

### <span data-ttu-id="646e6-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="646e6-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="646e6-139">筆記</span><span class="sxs-lookup"><span data-stu-id="646e6-139">NOTES</span></span>

## <span data-ttu-id="646e6-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="646e6-140">RELATED LINKS</span></span>
