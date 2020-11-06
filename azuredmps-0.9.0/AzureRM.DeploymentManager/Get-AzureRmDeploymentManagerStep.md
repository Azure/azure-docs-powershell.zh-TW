---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: bd17ee5dd653ee66daf014c57661b3787c04b06f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442603"
---
# <span data-ttu-id="b2f94-101">Get-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="b2f94-101">Get-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="b2f94-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b2f94-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f94-103">取得部署步驟。</span><span class="sxs-lookup"><span data-stu-id="b2f94-103">Gets the deployment step.</span></span>

## <span data-ttu-id="b2f94-104">句法</span><span class="sxs-lookup"><span data-stu-id="b2f94-104">SYNTAX</span></span>

### <span data-ttu-id="b2f94-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="b2f94-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2f94-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2f94-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2f94-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b2f94-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2f94-108">說明</span><span class="sxs-lookup"><span data-stu-id="b2f94-108">DESCRIPTION</span></span>
<span data-ttu-id="b2f94-109">**AzureRmDeploymentManagerStep** Cmdlet 會取得一個步驟，並傳回代表該步驟的物件。</span><span class="sxs-lookup"><span data-stu-id="b2f94-109">The **Get-AzureRmDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="b2f94-110">依其名稱和資源群組名稱來指定步驟。</span><span class="sxs-lookup"><span data-stu-id="b2f94-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="b2f94-111">或者，您也可以提供 Step 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="b2f94-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="b2f94-112">您可以在本機修改這個物件，然後使用 Set-AzureRmDeploymentManagerStep Cmdlet 將變更套用至專案來源。</span><span class="sxs-lookup"><span data-stu-id="b2f94-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="b2f94-113">示例</span><span class="sxs-lookup"><span data-stu-id="b2f94-113">EXAMPLES</span></span>

### <span data-ttu-id="b2f94-114">範例1：取得步驟</span><span class="sxs-lookup"><span data-stu-id="b2f94-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="b2f94-115">這個命令會在 ContosoResourceGroup 中取得名為 ContosoService1WaitStep 的步驟。</span><span class="sxs-lookup"><span data-stu-id="b2f94-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b2f94-116">範例2：使用資源識別碼取得步驟</span><span class="sxs-lookup"><span data-stu-id="b2f94-116">Example 2: Get a step using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="b2f94-117">這個命令會在 ContosoResourceGroup 中取得名為 ContosoService1WaitStep 的步驟。</span><span class="sxs-lookup"><span data-stu-id="b2f94-117">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b2f94-118">範例3：使用 New-AzureRmDeploymentManagerStep 傳回的物件來取得步驟</span><span class="sxs-lookup"><span data-stu-id="b2f94-118">Example 3: Get a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="b2f94-119">這個命令會分別取得 name 和 ResourceGroup 與 $stepObject 之 Name 和 ResourceGroupName 屬性相符的步驟。</span><span class="sxs-lookup"><span data-stu-id="b2f94-119">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>


## <span data-ttu-id="b2f94-120">參數</span><span class="sxs-lookup"><span data-stu-id="b2f94-120">PARAMETERS</span></span>

### <span data-ttu-id="b2f94-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f94-121">-DefaultProfile</span></span>
<span data-ttu-id="b2f94-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b2f94-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2f94-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="b2f94-123">-Name</span></span>
<span data-ttu-id="b2f94-124">步驟的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2f94-124">The name of the step.</span></span>

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

### <span data-ttu-id="b2f94-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2f94-125">-ResourceGroupName</span></span>
<span data-ttu-id="b2f94-126">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="b2f94-126">The resource group.</span></span>

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

### <span data-ttu-id="b2f94-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2f94-127">-ResourceId</span></span>
<span data-ttu-id="b2f94-128">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2f94-128">The resource identifier.</span></span>

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

### <span data-ttu-id="b2f94-129">-步驟</span><span class="sxs-lookup"><span data-stu-id="b2f94-129">-Step</span></span>
<span data-ttu-id="b2f94-130">[步驟資源] 物件。</span><span class="sxs-lookup"><span data-stu-id="b2f94-130">The step resource object.</span></span>

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

### <span data-ttu-id="b2f94-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f94-131">CommonParameters</span></span>
<span data-ttu-id="b2f94-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b2f94-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b2f94-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b2f94-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f94-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b2f94-134">INPUTS</span></span>

### <span data-ttu-id="b2f94-135">System.object</span><span class="sxs-lookup"><span data-stu-id="b2f94-135">System.String</span></span>

### <span data-ttu-id="b2f94-136">PSStepResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="b2f94-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="b2f94-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b2f94-137">OUTPUTS</span></span>

### <span data-ttu-id="b2f94-138">PSStepResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="b2f94-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="b2f94-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b2f94-139">NOTES</span></span>

## <span data-ttu-id="b2f94-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2f94-140">RELATED LINKS</span></span>
