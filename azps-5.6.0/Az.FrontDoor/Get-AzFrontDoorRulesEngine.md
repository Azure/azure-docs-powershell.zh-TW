---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 62ef80d7af7ce9b9a10a7a18b38fbf5c6f1db562
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912841"
---
# <span data-ttu-id="9c554-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="9c554-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="9c554-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9c554-102">SYNOPSIS</span></span>
<span data-ttu-id="9c554-103">取得規則引擎組配置。</span><span class="sxs-lookup"><span data-stu-id="9c554-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="9c554-104">語法</span><span class="sxs-lookup"><span data-stu-id="9c554-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c554-105">描述</span><span class="sxs-lookup"><span data-stu-id="9c554-105">DESCRIPTION</span></span>
<span data-ttu-id="9c554-106">**Get-AzFrontDoorRulesEngine Cmdlet** 會取得特定的規則引擎組式，或取得與前門關聯的所有規則引擎組式組。</span><span class="sxs-lookup"><span data-stu-id="9c554-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="9c554-107">例子</span><span class="sxs-lookup"><span data-stu-id="9c554-107">EXAMPLES</span></span>

### <span data-ttu-id="9c554-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="9c554-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="9c554-109">取得特定的規則引擎組。</span><span class="sxs-lookup"><span data-stu-id="9c554-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="9c554-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="9c554-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="9c554-111">在前門取得所有規則引擎組配置。</span><span class="sxs-lookup"><span data-stu-id="9c554-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="9c554-112">範例 3</span><span class="sxs-lookup"><span data-stu-id="9c554-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="9c554-113">取得不存在的規則引擎時的預期輸出。</span><span class="sxs-lookup"><span data-stu-id="9c554-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="9c554-114">參數</span><span class="sxs-lookup"><span data-stu-id="9c554-114">PARAMETERS</span></span>

### <span data-ttu-id="9c554-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c554-115">-DefaultProfile</span></span>
<span data-ttu-id="9c554-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c554-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c554-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="9c554-117">-FrontDoorName</span></span>
<span data-ttu-id="9c554-118">前門名稱。</span><span class="sxs-lookup"><span data-stu-id="9c554-118">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c554-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="9c554-119">-Name</span></span>
<span data-ttu-id="9c554-120">規則引擎名稱。</span><span class="sxs-lookup"><span data-stu-id="9c554-120">Rules engine name.</span></span>

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

### <span data-ttu-id="9c554-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c554-121">-ResourceGroupName</span></span>
<span data-ttu-id="9c554-122">要建立前門的資源組名。</span><span class="sxs-lookup"><span data-stu-id="9c554-122">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c554-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c554-123">CommonParameters</span></span>
<span data-ttu-id="9c554-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9c554-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c554-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c554-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c554-126">輸入</span><span class="sxs-lookup"><span data-stu-id="9c554-126">INPUTS</span></span>

### <span data-ttu-id="9c554-127">沒有</span><span class="sxs-lookup"><span data-stu-id="9c554-127">None</span></span>

## <span data-ttu-id="9c554-128">輸出</span><span class="sxs-lookup"><span data-stu-id="9c554-128">OUTPUTS</span></span>

### <span data-ttu-id="9c554-129">Microsoft.Azure.Commands.FrontDoor.models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="9c554-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="9c554-130">筆記</span><span class="sxs-lookup"><span data-stu-id="9c554-130">NOTES</span></span>

## <span data-ttu-id="9c554-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c554-131">RELATED LINKS</span></span>
