---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/get-azfunctionappavailablelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
ms.openlocfilehash: 987c4e351e024452231b5a5367ea7c2905d57863
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906194"
---
# <span data-ttu-id="63ae4-101">Get-AzFunctionAppAvailableLocation</span><span class="sxs-lookup"><span data-stu-id="63ae4-101">Get-AzFunctionAppAvailableLocation</span></span>

## <span data-ttu-id="63ae4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="63ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="63ae4-103">為指定作業系統和計畫類型提供函數應用程式的位置。</span><span class="sxs-lookup"><span data-stu-id="63ae4-103">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="63ae4-104">語法</span><span class="sxs-lookup"><span data-stu-id="63ae4-104">SYNTAX</span></span>

```
Get-AzFunctionAppAvailableLocation [[-SubscriptionId] <String[]>] [[-PlanType] <String>] [[-OSType] <String>]
 [[-DefaultProfile] <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="63ae4-105">描述</span><span class="sxs-lookup"><span data-stu-id="63ae4-105">DESCRIPTION</span></span>
<span data-ttu-id="63ae4-106">為指定作業系統和計畫類型提供函數應用程式的位置。</span><span class="sxs-lookup"><span data-stu-id="63ae4-106">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="63ae4-107">例子</span><span class="sxs-lookup"><span data-stu-id="63ae4-107">EXAMPLES</span></span>

### <span data-ttu-id="63ae4-108">範例 1：取得適用于 Windows 的 Premium 位置。</span><span class="sxs-lookup"><span data-stu-id="63ae4-108">Example 1: Get the locations where Premium is available for Windows.</span></span> <span data-ttu-id="63ae4-109">如果沒有指定參數，PlanType 會設為 'Premium'，OSType 則設為 'Windows'。</span><span class="sxs-lookup"><span data-stu-id="63ae4-109">If no parameters are specified, PlanType is set to 'Premium' and OSType is set to 'Windows'.</span></span>
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

<span data-ttu-id="63ae4-110">此命令會獲得 Windows 提供進一版的位置。</span><span class="sxs-lookup"><span data-stu-id="63ae4-110">This command gets the locations where Premium is available for Windows.</span></span>

### <span data-ttu-id="63ae4-111">範例 2：取得適用于 Linux 的 Premium 位置。</span><span class="sxs-lookup"><span data-stu-id="63ae4-111">Example 2: Get the locations where Premium is available for Linux.</span></span>
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

<span data-ttu-id="63ae4-112">此命令會獲得 Linux 提供進一版的位置。</span><span class="sxs-lookup"><span data-stu-id="63ae4-112">This command gets the locations where Premium is available for Linux.</span></span>

### <span data-ttu-id="63ae4-113">範例 3：取得 Windows 可用的消費位置。</span><span class="sxs-lookup"><span data-stu-id="63ae4-113">Example 3: Get the locations where Consumption is available for Windows.</span></span>
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

<span data-ttu-id="63ae4-114">此命令會獲得 Windows 可用的消費位置。</span><span class="sxs-lookup"><span data-stu-id="63ae4-114">This command gets the locations where Consumption is available for Windows.</span></span>

## <span data-ttu-id="63ae4-115">參數</span><span class="sxs-lookup"><span data-stu-id="63ae4-115">PARAMETERS</span></span>

### <span data-ttu-id="63ae4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63ae4-116">-DefaultProfile</span></span>
<span data-ttu-id="63ae4-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="63ae4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63ae4-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="63ae4-118">-OSType</span></span>
<span data-ttu-id="63ae4-119">服務方案的作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="63ae4-119">The OS type for the service plan.</span></span>

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

### <span data-ttu-id="63ae4-120">-PlanType</span><span class="sxs-lookup"><span data-stu-id="63ae4-120">-PlanType</span></span>
<span data-ttu-id="63ae4-121">計畫類型。</span><span class="sxs-lookup"><span data-stu-id="63ae4-121">The plan type.</span></span>
<span data-ttu-id="63ae4-122">有效輸入：消費或進一步</span><span class="sxs-lookup"><span data-stu-id="63ae4-122">Valid inputs: Consumption or Premium</span></span>

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

### <span data-ttu-id="63ae4-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="63ae4-123">-SubscriptionId</span></span>
<span data-ttu-id="63ae4-124">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="63ae4-124">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="63ae4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63ae4-125">CommonParameters</span></span>
<span data-ttu-id="63ae4-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="63ae4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63ae4-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63ae4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63ae4-128">輸入</span><span class="sxs-lookup"><span data-stu-id="63ae4-128">INPUTS</span></span>

## <span data-ttu-id="63ae4-129">輸出</span><span class="sxs-lookup"><span data-stu-id="63ae4-129">OUTPUTS</span></span>

### <span data-ttu-id="63ae4-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.models.Api20190801.IGeoRegion</span><span class="sxs-lookup"><span data-stu-id="63ae4-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span></span>

## <span data-ttu-id="63ae4-131">筆記</span><span class="sxs-lookup"><span data-stu-id="63ae4-131">NOTES</span></span>

<span data-ttu-id="63ae4-132">別名</span><span class="sxs-lookup"><span data-stu-id="63ae4-132">ALIASES</span></span>

## <span data-ttu-id="63ae4-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="63ae4-133">RELATED LINKS</span></span>

