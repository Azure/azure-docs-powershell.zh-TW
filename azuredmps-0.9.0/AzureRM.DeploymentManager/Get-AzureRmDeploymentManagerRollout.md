---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 21d0b4f7feec5b32ff732f880924becddd84db73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442348"
---
# <span data-ttu-id="22e09-101">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="22e09-101">Get-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="22e09-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22e09-102">SYNOPSIS</span></span>
<span data-ttu-id="22e09-103">取得推出。</span><span class="sxs-lookup"><span data-stu-id="22e09-103">Gets a rollout.</span></span>

## <span data-ttu-id="22e09-104">句法</span><span class="sxs-lookup"><span data-stu-id="22e09-104">SYNTAX</span></span>

### <span data-ttu-id="22e09-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="22e09-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [[-RetryAttempt] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22e09-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="22e09-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22e09-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="22e09-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22e09-108">說明</span><span class="sxs-lookup"><span data-stu-id="22e09-108">DESCRIPTION</span></span>
<span data-ttu-id="22e09-109">**AzureRmDeploymentManagerRollout** Cmdlet 會取得推出，並傳回一個物件，該物件代表有關推出進度之所有詳細資訊的推出。</span><span class="sxs-lookup"><span data-stu-id="22e09-109">The **Get-AzureRmDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="22e09-110">依其名稱和資源群組名稱來指定推出。</span><span class="sxs-lookup"><span data-stu-id="22e09-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="22e09-111">或者，您也可以提供推出物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="22e09-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="22e09-112">示例</span><span class="sxs-lookup"><span data-stu-id="22e09-112">EXAMPLES</span></span>

### <span data-ttu-id="22e09-113">範例1</span><span class="sxs-lookup"><span data-stu-id="22e09-113">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="22e09-114">這個命令會在 ContosoResourceGroup 中取得名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="22e09-114">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="22e09-115">範例2：使用資源識別碼取得推出</span><span class="sxs-lookup"><span data-stu-id="22e09-115">Example 2: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="22e09-116">這個命令會在 ContosoResourceGroup 中取得名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="22e09-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="22e09-117">範例3：使用 [推出] 物件取得推出。</span><span class="sxs-lookup"><span data-stu-id="22e09-117">Example 3: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="22e09-118">這個命令會分別取得名稱和 ResourceGroup 與 $rolloutObject 之 Name 和 ResourceGroupName 屬性相符的推出。</span><span class="sxs-lookup"><span data-stu-id="22e09-118">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="22e09-119">參數</span><span class="sxs-lookup"><span data-stu-id="22e09-119">PARAMETERS</span></span>

### <span data-ttu-id="22e09-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e09-120">-DefaultProfile</span></span>
<span data-ttu-id="22e09-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="22e09-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e09-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="22e09-122">-Name</span></span>
<span data-ttu-id="22e09-123">推出的名稱。</span><span class="sxs-lookup"><span data-stu-id="22e09-123">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e09-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22e09-124">-ResourceGroupName</span></span>
<span data-ttu-id="22e09-125">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="22e09-125">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e09-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22e09-126">-ResourceId</span></span>
<span data-ttu-id="22e09-127">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="22e09-127">The resource identifier.</span></span>

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

### <span data-ttu-id="22e09-128">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="22e09-128">-RetryAttempt</span></span>
<span data-ttu-id="22e09-129">首次嘗試嘗試。</span><span class="sxs-lookup"><span data-stu-id="22e09-129">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e09-130">-推出</span><span class="sxs-lookup"><span data-stu-id="22e09-130">-Rollout</span></span>
<span data-ttu-id="22e09-131">推出物件。</span><span class="sxs-lookup"><span data-stu-id="22e09-131">Rollout object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22e09-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e09-132">CommonParameters</span></span>
<span data-ttu-id="22e09-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22e09-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e09-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="22e09-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e09-135">輸入</span><span class="sxs-lookup"><span data-stu-id="22e09-135">INPUTS</span></span>

### <span data-ttu-id="22e09-136">所有</span><span class="sxs-lookup"><span data-stu-id="22e09-136">None</span></span>

## <span data-ttu-id="22e09-137">輸出</span><span class="sxs-lookup"><span data-stu-id="22e09-137">OUTPUTS</span></span>

### <span data-ttu-id="22e09-138">PSRollout 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="22e09-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="22e09-139">筆記</span><span class="sxs-lookup"><span data-stu-id="22e09-139">NOTES</span></span>

## <span data-ttu-id="22e09-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="22e09-140">RELATED LINKS</span></span>

[<span data-ttu-id="22e09-141">停止 AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="22e09-141">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="22e09-142">重新開機-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="22e09-142">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="22e09-143">移除-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="22e09-143">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)