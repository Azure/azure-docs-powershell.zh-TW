---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: 68bc2af69c3450f0c52c5613057ba4b2db211ee8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128225"
---
# <span data-ttu-id="89d53-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="89d53-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="89d53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89d53-102">SYNOPSIS</span></span>
<span data-ttu-id="89d53-103">取得步驟。</span><span class="sxs-lookup"><span data-stu-id="89d53-103">Gets the step.</span></span>

## <span data-ttu-id="89d53-104">句法</span><span class="sxs-lookup"><span data-stu-id="89d53-104">SYNTAX</span></span>

### <span data-ttu-id="89d53-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="89d53-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89d53-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="89d53-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="89d53-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="89d53-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89d53-108">說明</span><span class="sxs-lookup"><span data-stu-id="89d53-108">DESCRIPTION</span></span>
<span data-ttu-id="89d53-109">**AzDeploymentManagerStep** Cmdlet 會取得一個步驟，並傳回代表該步驟的物件。</span><span class="sxs-lookup"><span data-stu-id="89d53-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="89d53-110">依其名稱和資源群組名稱來指定步驟。</span><span class="sxs-lookup"><span data-stu-id="89d53-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="89d53-111">或者，您也可以提供 Step 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="89d53-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="89d53-112">您可以在本機修改這個物件，然後使用 Set-AzDeploymentManagerStep Cmdlet 將變更套用至專案來源。</span><span class="sxs-lookup"><span data-stu-id="89d53-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="89d53-113">示例</span><span class="sxs-lookup"><span data-stu-id="89d53-113">EXAMPLES</span></span>

### <span data-ttu-id="89d53-114">範例1：取得步驟</span><span class="sxs-lookup"><span data-stu-id="89d53-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="89d53-115">這個命令會在 ContosoResourceGroup 中取得名為 ContosoService1WaitStep 的步驟。</span><span class="sxs-lookup"><span data-stu-id="89d53-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="89d53-116">範例2：使用資源識別碼取得步驟</span><span class="sxs-lookup"><span data-stu-id="89d53-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="89d53-117">範例1</span><span class="sxs-lookup"><span data-stu-id="89d53-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="89d53-118">這個命令會在 ContosoResourceGroup 中取得名為 ContosoService1WaitStep 的步驟。</span><span class="sxs-lookup"><span data-stu-id="89d53-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="89d53-119">範例3：使用 New-AzDeploymentManagerStep 傳回的物件來取得步驟</span><span class="sxs-lookup"><span data-stu-id="89d53-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="89d53-120">這個命令會分別取得 name 和 ResourceGroup 與 $stepObject 之 Name 和 ResourceGroupName 屬性相符的步驟。</span><span class="sxs-lookup"><span data-stu-id="89d53-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="89d53-121">參數</span><span class="sxs-lookup"><span data-stu-id="89d53-121">PARAMETERS</span></span>

### <span data-ttu-id="89d53-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89d53-122">-DefaultProfile</span></span>
<span data-ttu-id="89d53-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="89d53-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89d53-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89d53-124">-InputObject</span></span>
<span data-ttu-id="89d53-125">[步驟資源] 物件。</span><span class="sxs-lookup"><span data-stu-id="89d53-125">The step resource object.</span></span>

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

### <span data-ttu-id="89d53-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="89d53-126">-Name</span></span>
<span data-ttu-id="89d53-127">步驟的名稱。</span><span class="sxs-lookup"><span data-stu-id="89d53-127">The name of the step.</span></span>

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

### <span data-ttu-id="89d53-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89d53-128">-ResourceGroupName</span></span>
<span data-ttu-id="89d53-129">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="89d53-129">The resource group.</span></span>

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

### <span data-ttu-id="89d53-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89d53-130">-ResourceId</span></span>
<span data-ttu-id="89d53-131">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="89d53-131">The resource identifier.</span></span>

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

### <span data-ttu-id="89d53-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89d53-132">CommonParameters</span></span>
<span data-ttu-id="89d53-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89d53-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89d53-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="89d53-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89d53-135">輸入</span><span class="sxs-lookup"><span data-stu-id="89d53-135">INPUTS</span></span>

### <span data-ttu-id="89d53-136">System.object</span><span class="sxs-lookup"><span data-stu-id="89d53-136">System.String</span></span>

### <span data-ttu-id="89d53-137">PSStepResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="89d53-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="89d53-138">輸出</span><span class="sxs-lookup"><span data-stu-id="89d53-138">OUTPUTS</span></span>

### <span data-ttu-id="89d53-139">PSStepResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="89d53-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="89d53-140">筆記</span><span class="sxs-lookup"><span data-stu-id="89d53-140">NOTES</span></span>

## <span data-ttu-id="89d53-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="89d53-141">RELATED LINKS</span></span>
