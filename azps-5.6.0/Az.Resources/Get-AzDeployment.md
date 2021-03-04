---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 92a0aac5043be520f6a7ed7afc2066e0532b79ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903953"
---
# <span data-ttu-id="3e7d2-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="3e7d2-101">Get-AzDeployment</span></span>

## <span data-ttu-id="3e7d2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3e7d2-102">SYNOPSIS</span></span>
<span data-ttu-id="3e7d2-103">取得部署</span><span class="sxs-lookup"><span data-stu-id="3e7d2-103">Get deployment</span></span>

## <span data-ttu-id="3e7d2-104">語法</span><span class="sxs-lookup"><span data-stu-id="3e7d2-104">SYNTAX</span></span>

### <span data-ttu-id="3e7d2-105">GetByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="3e7d2-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e7d2-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="3e7d2-106">GetByDeploymentId</span></span>
```
Get-AzDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e7d2-107">描述</span><span class="sxs-lookup"><span data-stu-id="3e7d2-107">DESCRIPTION</span></span>
<span data-ttu-id="3e7d2-108">**Get-AzDeployment** Cmdlet 會取得目前訂閱範圍中的部署。</span><span class="sxs-lookup"><span data-stu-id="3e7d2-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="3e7d2-109">指定 *名稱* 或 *Id* 參數以篩選結果。</span><span class="sxs-lookup"><span data-stu-id="3e7d2-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="3e7d2-110">根據預設 **，Get-AzDeployment** 會取得目前訂閱範圍的所有部署。</span><span class="sxs-lookup"><span data-stu-id="3e7d2-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="3e7d2-111">例子</span><span class="sxs-lookup"><span data-stu-id="3e7d2-111">EXAMPLES</span></span>

### <span data-ttu-id="3e7d2-112">範例 1：取得訂閱範圍的所有部署</span><span class="sxs-lookup"><span data-stu-id="3e7d2-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="3e7d2-113">此命令會獲得目前訂閱範圍的所有部署。</span><span class="sxs-lookup"><span data-stu-id="3e7d2-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="3e7d2-114">範例 2：根據名稱取得部署</span><span class="sxs-lookup"><span data-stu-id="3e7d2-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="3e7d2-115">此命令會以目前的訂閱範圍來部署 DeployRoles01。</span><span class="sxs-lookup"><span data-stu-id="3e7d2-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="3e7d2-116">您可以使用 **New-AzDeployment** Cmdlet 為部署建立時指派名稱。</span><span class="sxs-lookup"><span data-stu-id="3e7d2-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="3e7d2-117">如果您沒有指派名稱，Cmdlet 會根據用來建立部署的範本提供預設名稱。</span><span class="sxs-lookup"><span data-stu-id="3e7d2-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="3e7d2-118">參數</span><span class="sxs-lookup"><span data-stu-id="3e7d2-118">PARAMETERS</span></span>

### <span data-ttu-id="3e7d2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e7d2-119">-DefaultProfile</span></span>
<span data-ttu-id="3e7d2-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e7d2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e7d2-121">-Id</span><span class="sxs-lookup"><span data-stu-id="3e7d2-121">-Id</span></span>
<span data-ttu-id="3e7d2-122">部署之完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e7d2-122">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="3e7d2-123">範例：/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="3e7d2-123">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="3e7d2-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e7d2-124">-Name</span></span>
<span data-ttu-id="3e7d2-125">部署名稱。</span><span class="sxs-lookup"><span data-stu-id="3e7d2-125">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e7d2-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="3e7d2-126">-Pre</span></span>
<span data-ttu-id="3e7d2-127">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="3e7d2-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3e7d2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e7d2-128">CommonParameters</span></span>
<span data-ttu-id="3e7d2-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3e7d2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e7d2-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e7d2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e7d2-131">輸入</span><span class="sxs-lookup"><span data-stu-id="3e7d2-131">INPUTS</span></span>

### <span data-ttu-id="3e7d2-132">沒有</span><span class="sxs-lookup"><span data-stu-id="3e7d2-132">None</span></span>

## <span data-ttu-id="3e7d2-133">輸出</span><span class="sxs-lookup"><span data-stu-id="3e7d2-133">OUTPUTS</span></span>

### <span data-ttu-id="3e7d2-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="3e7d2-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="3e7d2-135">筆記</span><span class="sxs-lookup"><span data-stu-id="3e7d2-135">NOTES</span></span>

## <span data-ttu-id="3e7d2-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e7d2-136">RELATED LINKS</span></span>
