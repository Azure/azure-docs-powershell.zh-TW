---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappavailablelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
ms.openlocfilehash: 3ab2ab4778b7fdb12334db416c953a7c373c63b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143083"
---
# <span data-ttu-id="a5f51-101">Get-AzFunctionAppAvailableLocation</span><span class="sxs-lookup"><span data-stu-id="a5f51-101">Get-AzFunctionAppAvailableLocation</span></span>

## <span data-ttu-id="a5f51-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5f51-102">SYNOPSIS</span></span>
<span data-ttu-id="a5f51-103">取得給定 os 和方案類型的函數應用程式在哪個位置可用。</span><span class="sxs-lookup"><span data-stu-id="a5f51-103">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="a5f51-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5f51-104">SYNTAX</span></span>

```
Get-AzFunctionAppAvailableLocation [[-SubscriptionId] <String[]>] [[-PlanType] <String>] [[-OSType] <String>]
 [[-DefaultProfile] <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a5f51-105">說明</span><span class="sxs-lookup"><span data-stu-id="a5f51-105">DESCRIPTION</span></span>
<span data-ttu-id="a5f51-106">取得給定 os 和方案類型的函數應用程式在哪個位置可用。</span><span class="sxs-lookup"><span data-stu-id="a5f51-106">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="a5f51-107">示例</span><span class="sxs-lookup"><span data-stu-id="a5f51-107">EXAMPLES</span></span>

### <span data-ttu-id="a5f51-108">範例1：取得可在 Windows 中使用 Premium 的位置。</span><span class="sxs-lookup"><span data-stu-id="a5f51-108">Example 1: Get the locations where Premium is available for Windows.</span></span> <span data-ttu-id="a5f51-109">如果未指定任何參數，PlanType 會設定為 "Premium"，而 OSType 則會設定為 [Windows]。</span><span class="sxs-lookup"><span data-stu-id="a5f51-109">If no parameters are specified, PlanType is set to 'Premium' and OSType is set to 'Windows'.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
West India
South India
Canada Central
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
Germany West Central
Norway East
```

<span data-ttu-id="a5f51-110">這個命令會取得可在 Windows 中使用 Premium 的位置。</span><span class="sxs-lookup"><span data-stu-id="a5f51-110">This command gets the locations where Premium is available for Windows.</span></span>

### <span data-ttu-id="a5f51-111">範例2：取得可在 Linux 中使用 Premium 的位置。</span><span class="sxs-lookup"><span data-stu-id="a5f51-111">Example 2: Get the locations where Premium is available for Linux.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Premium -OSType Linux

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
West India
Canada Central
West Central US
West US 2
UK West
UK South
Central US EUAP
Korea Central
France Central
Norway East
```

<span data-ttu-id="a5f51-112">這個命令會取得可在 Linux 中使用 Premium 的位置。</span><span class="sxs-lookup"><span data-stu-id="a5f51-112">This command gets the locations where Premium is available for Linux.</span></span>

### <span data-ttu-id="a5f51-113">範例3：取得可用於 Windows 的消耗量位置。</span><span class="sxs-lookup"><span data-stu-id="a5f51-113">Example 3: Get the locations where Consumption is available for Windows.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Consumption -OSType Windows

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
Central India
West India
South India
Canada Central
Canada East
West Central US
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
South Africa North
Switzerland North
Germany West Central
```

<span data-ttu-id="a5f51-114">這個命令會取得可供 Windows 使用的位置。</span><span class="sxs-lookup"><span data-stu-id="a5f51-114">This command gets the locations where Consumption is available for Windows.</span></span>

## <span data-ttu-id="a5f51-115">參數</span><span class="sxs-lookup"><span data-stu-id="a5f51-115">PARAMETERS</span></span>

### <span data-ttu-id="a5f51-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5f51-116">-DefaultProfile</span></span>
<span data-ttu-id="a5f51-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5f51-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f51-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="a5f51-118">-OSType</span></span>
<span data-ttu-id="a5f51-119">服務方案的 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="a5f51-119">The OS type for the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f51-120">-PlanType</span><span class="sxs-lookup"><span data-stu-id="a5f51-120">-PlanType</span></span>
<span data-ttu-id="a5f51-121">方案類型。</span><span class="sxs-lookup"><span data-stu-id="a5f51-121">The plan type.</span></span>
<span data-ttu-id="a5f51-122">有效輸入：消耗量或津貼</span><span class="sxs-lookup"><span data-stu-id="a5f51-122">Valid inputs: Consumption or Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f51-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5f51-123">-SubscriptionId</span></span>
<span data-ttu-id="a5f51-124">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="a5f51-124">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f51-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5f51-125">CommonParameters</span></span>
<span data-ttu-id="a5f51-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5f51-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5f51-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a5f51-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5f51-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a5f51-128">INPUTS</span></span>

## <span data-ttu-id="a5f51-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a5f51-129">OUTPUTS</span></span>

### <span data-ttu-id="a5f51-130">IGeoRegion 中的 Api20190801，然後再</span><span class="sxs-lookup"><span data-stu-id="a5f51-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span></span>

## <span data-ttu-id="a5f51-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a5f51-131">NOTES</span></span>

<span data-ttu-id="a5f51-132">別名</span><span class="sxs-lookup"><span data-stu-id="a5f51-132">ALIASES</span></span>

## <span data-ttu-id="a5f51-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5f51-133">RELATED LINKS</span></span>

