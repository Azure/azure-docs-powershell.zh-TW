---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: 5bf59cb766d82e2fc50bdc75c0a072e2b8d17a69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905509"
---
# <span data-ttu-id="b73d5-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="b73d5-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="b73d5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b73d5-102">SYNOPSIS</span></span>
<span data-ttu-id="b73d5-103">完成步驟。</span><span class="sxs-lookup"><span data-stu-id="b73d5-103">Gets the step.</span></span>

## <span data-ttu-id="b73d5-104">語法</span><span class="sxs-lookup"><span data-stu-id="b73d5-104">SYNTAX</span></span>

### <span data-ttu-id="b73d5-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="b73d5-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b73d5-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b73d5-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b73d5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b73d5-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b73d5-108">描述</span><span class="sxs-lookup"><span data-stu-id="b73d5-108">DESCRIPTION</span></span>
<span data-ttu-id="b73d5-109">**Get-AzDeploymentManagerStep** Cmdlet 會取得一個步驟，並會返回代表該步驟的物件。</span><span class="sxs-lookup"><span data-stu-id="b73d5-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="b73d5-110">根據步驟的名稱和資源組名來指定步驟。</span><span class="sxs-lookup"><span data-stu-id="b73d5-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="b73d5-111">或者，您也可以提供 Step 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="b73d5-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="b73d5-112">您可以在本地修改此物件，然後使用 Cmdlet 將變更Set-AzDeploymentManagerStep來源。</span><span class="sxs-lookup"><span data-stu-id="b73d5-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="b73d5-113">例子</span><span class="sxs-lookup"><span data-stu-id="b73d5-113">EXAMPLES</span></span>

### <span data-ttu-id="b73d5-114">範例 1：取得步驟</span><span class="sxs-lookup"><span data-stu-id="b73d5-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="b73d5-115">此命令會獲得 ContosoResourceGroup 中名為 ContosoService1WaitStep 的步驟。</span><span class="sxs-lookup"><span data-stu-id="b73d5-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b73d5-116">範例 2：使用資源識別碼取得步驟</span><span class="sxs-lookup"><span data-stu-id="b73d5-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="b73d5-117">範例 1</span><span class="sxs-lookup"><span data-stu-id="b73d5-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="b73d5-118">此命令會獲得 ContosoResourceGroup 中名為 ContosoService1WaitStep 的步驟。</span><span class="sxs-lookup"><span data-stu-id="b73d5-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b73d5-119">範例 3：使用由 New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="b73d5-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="b73d5-120">此命令會獲得一個步驟，其名稱和資源組會分別符合該名稱及$stepObject屬性。</span><span class="sxs-lookup"><span data-stu-id="b73d5-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="b73d5-121">參數</span><span class="sxs-lookup"><span data-stu-id="b73d5-121">PARAMETERS</span></span>

### <span data-ttu-id="b73d5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b73d5-122">-DefaultProfile</span></span>
<span data-ttu-id="b73d5-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b73d5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b73d5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b73d5-124">-InputObject</span></span>
<span data-ttu-id="b73d5-125">步驟資源物件。</span><span class="sxs-lookup"><span data-stu-id="b73d5-125">The step resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b73d5-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="b73d5-126">-Name</span></span>
<span data-ttu-id="b73d5-127">步驟的名稱。</span><span class="sxs-lookup"><span data-stu-id="b73d5-127">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b73d5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b73d5-128">-ResourceGroupName</span></span>
<span data-ttu-id="b73d5-129">資源群組。</span><span class="sxs-lookup"><span data-stu-id="b73d5-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b73d5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b73d5-130">-ResourceId</span></span>
<span data-ttu-id="b73d5-131">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b73d5-131">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b73d5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b73d5-132">CommonParameters</span></span>
<span data-ttu-id="b73d5-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b73d5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b73d5-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b73d5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b73d5-135">輸入</span><span class="sxs-lookup"><span data-stu-id="b73d5-135">INPUTS</span></span>

### <span data-ttu-id="b73d5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b73d5-136">System.String</span></span>

### <span data-ttu-id="b73d5-137">Microsoft.Azure.Commands.DeploymentManager.models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="b73d5-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="b73d5-138">輸出</span><span class="sxs-lookup"><span data-stu-id="b73d5-138">OUTPUTS</span></span>

### <span data-ttu-id="b73d5-139">Microsoft.Azure.Commands.DeploymentManager.models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="b73d5-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="b73d5-140">筆記</span><span class="sxs-lookup"><span data-stu-id="b73d5-140">NOTES</span></span>

## <span data-ttu-id="b73d5-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b73d5-141">RELATED LINKS</span></span>
