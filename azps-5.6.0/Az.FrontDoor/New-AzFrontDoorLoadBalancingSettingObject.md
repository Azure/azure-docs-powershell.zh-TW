---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: 840c4db17e81f93fc40c86f7c22129b570583bd5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906670"
---
# <span data-ttu-id="11031-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="11031-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="11031-102">簡介</span><span class="sxs-lookup"><span data-stu-id="11031-102">SYNOPSIS</span></span>
<span data-ttu-id="11031-103">建立 PSLoadBalsettingSetting 物件以建立前端門</span><span class="sxs-lookup"><span data-stu-id="11031-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="11031-104">語法</span><span class="sxs-lookup"><span data-stu-id="11031-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11031-105">描述</span><span class="sxs-lookup"><span data-stu-id="11031-105">DESCRIPTION</span></span>
<span data-ttu-id="11031-106">建立 PSLoadBalsettingSetting 物件以建立前端門</span><span class="sxs-lookup"><span data-stu-id="11031-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="11031-107">例子</span><span class="sxs-lookup"><span data-stu-id="11031-107">EXAMPLES</span></span>

### <span data-ttu-id="11031-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="11031-108">Example 1</span></span>
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

<span data-ttu-id="11031-109">建立 PSLoadBalsettingSetting 物件以建立前端門</span><span class="sxs-lookup"><span data-stu-id="11031-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="11031-110">參數</span><span class="sxs-lookup"><span data-stu-id="11031-110">PARAMETERS</span></span>

### <span data-ttu-id="11031-111">-AdditionalLatencyInMilli秒s</span><span class="sxs-lookup"><span data-stu-id="11031-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="11031-112">額外的延遲時間 ，以毫秒為單位，讓探索進入最低延遲的容器。</span><span class="sxs-lookup"><span data-stu-id="11031-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="11031-113">預設值為 0</span><span class="sxs-lookup"><span data-stu-id="11031-113">Default value is 0</span></span>

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

### <span data-ttu-id="11031-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11031-114">-DefaultProfile</span></span>
<span data-ttu-id="11031-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="11031-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11031-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="11031-116">-Name</span></span>
<span data-ttu-id="11031-117">健康值設定名稱。</span><span class="sxs-lookup"><span data-stu-id="11031-117">health probe setting name.</span></span>

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

### <span data-ttu-id="11031-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="11031-118">-SampleSize</span></span>
<span data-ttu-id="11031-119">要決定負載平衡的考慮樣本數目。</span><span class="sxs-lookup"><span data-stu-id="11031-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="11031-120">預設值為 4</span><span class="sxs-lookup"><span data-stu-id="11031-120">Default value is 4</span></span>

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

### <span data-ttu-id="11031-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="11031-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="11031-122">樣本週期內必須成功之預設值的樣本數為 2</span><span class="sxs-lookup"><span data-stu-id="11031-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="11031-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11031-123">CommonParameters</span></span>
<span data-ttu-id="11031-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="11031-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11031-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11031-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11031-126">輸入</span><span class="sxs-lookup"><span data-stu-id="11031-126">INPUTS</span></span>

### <span data-ttu-id="11031-127">沒有</span><span class="sxs-lookup"><span data-stu-id="11031-127">None</span></span>

## <span data-ttu-id="11031-128">輸出</span><span class="sxs-lookup"><span data-stu-id="11031-128">OUTPUTS</span></span>

### <span data-ttu-id="11031-129">Microsoft.Azure.Commands.FrontDoor.models.PSLoadBalsettingSetting</span><span class="sxs-lookup"><span data-stu-id="11031-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="11031-130">筆記</span><span class="sxs-lookup"><span data-stu-id="11031-130">NOTES</span></span>

## <span data-ttu-id="11031-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="11031-131">RELATED LINKS</span></span>

<span data-ttu-id="11031-132">[New-AzFrontDoor](./New-AzFrontDoor.md) 
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="11031-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
