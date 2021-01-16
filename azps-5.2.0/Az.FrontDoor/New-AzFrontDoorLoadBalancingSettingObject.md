---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: e9195a60b06f206a5b3133834f19cfdab68db31b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274175"
---
# <span data-ttu-id="f3023-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="f3023-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="f3023-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3023-102">SYNOPSIS</span></span>
<span data-ttu-id="f3023-103">建立用來建立前門的 PSLoadBalancingSetting 物件</span><span class="sxs-lookup"><span data-stu-id="f3023-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="f3023-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3023-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3023-105">說明</span><span class="sxs-lookup"><span data-stu-id="f3023-105">DESCRIPTION</span></span>
<span data-ttu-id="f3023-106">建立用來建立前門的 PSLoadBalancingSetting 物件</span><span class="sxs-lookup"><span data-stu-id="f3023-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="f3023-107">示例</span><span class="sxs-lookup"><span data-stu-id="f3023-107">EXAMPLES</span></span>

### <span data-ttu-id="f3023-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f3023-108">Example 1</span></span>
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

<span data-ttu-id="f3023-109">建立用來建立前門的 PSLoadBalancingSetting 物件</span><span class="sxs-lookup"><span data-stu-id="f3023-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="f3023-110">參數</span><span class="sxs-lookup"><span data-stu-id="f3023-110">PARAMETERS</span></span>

### <span data-ttu-id="f3023-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="f3023-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="f3023-112">探測器落在最低延遲桶中的額外延遲（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f3023-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="f3023-113">預設值為0</span><span class="sxs-lookup"><span data-stu-id="f3023-113">Default value is 0</span></span>

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

### <span data-ttu-id="f3023-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3023-114">-DefaultProfile</span></span>
<span data-ttu-id="f3023-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3023-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3023-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3023-116">-Name</span></span>
<span data-ttu-id="f3023-117">health 探測設定名稱。</span><span class="sxs-lookup"><span data-stu-id="f3023-117">health probe setting name.</span></span>

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

### <span data-ttu-id="f3023-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="f3023-118">-SampleSize</span></span>
<span data-ttu-id="f3023-119">要考慮負載平衡決定的樣本數。</span><span class="sxs-lookup"><span data-stu-id="f3023-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="f3023-120">預設值為4</span><span class="sxs-lookup"><span data-stu-id="f3023-120">Default value is 4</span></span>

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

### <span data-ttu-id="f3023-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="f3023-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="f3023-122">範例期間內必須成功的範例數預設值為2</span><span class="sxs-lookup"><span data-stu-id="f3023-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="f3023-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3023-123">CommonParameters</span></span>
<span data-ttu-id="f3023-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3023-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3023-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f3023-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3023-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f3023-126">INPUTS</span></span>

### <span data-ttu-id="f3023-127">所有</span><span class="sxs-lookup"><span data-stu-id="f3023-127">None</span></span>

## <span data-ttu-id="f3023-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f3023-128">OUTPUTS</span></span>

### <span data-ttu-id="f3023-129">PSLoadBalancingSetting 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="f3023-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="f3023-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f3023-130">NOTES</span></span>

## <span data-ttu-id="f3023-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3023-131">RELATED LINKS</span></span>

<span data-ttu-id="f3023-132">[新-AzFrontDoor](./New-AzFrontDoor.md) 
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="f3023-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
