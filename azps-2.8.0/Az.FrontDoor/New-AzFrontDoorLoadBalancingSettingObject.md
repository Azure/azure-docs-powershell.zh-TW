---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: a1e5c02c1764d9d5284e28c8921ef09888a9d245
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612364"
---
# <span data-ttu-id="ef130-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="ef130-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="ef130-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef130-102">SYNOPSIS</span></span>
<span data-ttu-id="ef130-103">建立用來建立前門的 PSLoadBalancingSetting 物件</span><span class="sxs-lookup"><span data-stu-id="ef130-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="ef130-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef130-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef130-105">說明</span><span class="sxs-lookup"><span data-stu-id="ef130-105">DESCRIPTION</span></span>
<span data-ttu-id="ef130-106">建立用來建立前門的 PSLoadBalancingSetting 物件</span><span class="sxs-lookup"><span data-stu-id="ef130-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="ef130-107">示例</span><span class="sxs-lookup"><span data-stu-id="ef130-107">EXAMPLES</span></span>

### <span data-ttu-id="ef130-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ef130-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="ef130-109">建立用來建立前門的 PSLoadBalancingSetting 物件</span><span class="sxs-lookup"><span data-stu-id="ef130-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="ef130-110">參數</span><span class="sxs-lookup"><span data-stu-id="ef130-110">PARAMETERS</span></span>

### <span data-ttu-id="ef130-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="ef130-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="ef130-112">探測器落在最低延遲桶中的額外延遲（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ef130-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="ef130-113">預設值為0</span><span class="sxs-lookup"><span data-stu-id="ef130-113">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef130-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef130-114">-DefaultProfile</span></span>
<span data-ttu-id="ef130-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef130-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef130-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef130-116">-Name</span></span>
<span data-ttu-id="ef130-117">health 探測設定名稱。</span><span class="sxs-lookup"><span data-stu-id="ef130-117">health probe setting name.</span></span>

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

### <span data-ttu-id="ef130-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="ef130-118">-SampleSize</span></span>
<span data-ttu-id="ef130-119">要考慮負載平衡決定的樣本數。</span><span class="sxs-lookup"><span data-stu-id="ef130-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="ef130-120">預設值為4</span><span class="sxs-lookup"><span data-stu-id="ef130-120">Default value is 4</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef130-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="ef130-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="ef130-122">範例期間內必須成功的範例數預設值為2</span><span class="sxs-lookup"><span data-stu-id="ef130-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef130-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef130-123">CommonParameters</span></span>
<span data-ttu-id="ef130-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef130-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef130-125">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ef130-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef130-126">輸入</span><span class="sxs-lookup"><span data-stu-id="ef130-126">INPUTS</span></span>

### <span data-ttu-id="ef130-127">所有</span><span class="sxs-lookup"><span data-stu-id="ef130-127">None</span></span>

## <span data-ttu-id="ef130-128">輸出</span><span class="sxs-lookup"><span data-stu-id="ef130-128">OUTPUTS</span></span>

### <span data-ttu-id="ef130-129">PSLoadBalancingSetting 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="ef130-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="ef130-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ef130-130">NOTES</span></span>

## <span data-ttu-id="ef130-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef130-131">RELATED LINKS</span></span>

<span data-ttu-id="ef130-132">[新-AzFrontDoor](./New-AzFrontDoor.md) 
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="ef130-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
