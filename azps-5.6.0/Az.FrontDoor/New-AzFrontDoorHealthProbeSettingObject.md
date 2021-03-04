---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 4d65985d724033244f761748634adb3b2002a199
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906677"
---
# <span data-ttu-id="825d9-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="825d9-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="825d9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="825d9-102">SYNOPSIS</span></span>
<span data-ttu-id="825d9-103">建立 PSHealthProbeSetting 物件以用於建立前門</span><span class="sxs-lookup"><span data-stu-id="825d9-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="825d9-104">語法</span><span class="sxs-lookup"><span data-stu-id="825d9-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="825d9-105">描述</span><span class="sxs-lookup"><span data-stu-id="825d9-105">DESCRIPTION</span></span>
<span data-ttu-id="825d9-106">建立 PSHealthProbeSetting 物件以用於建立前門</span><span class="sxs-lookup"><span data-stu-id="825d9-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="825d9-107">例子</span><span class="sxs-lookup"><span data-stu-id="825d9-107">EXAMPLES</span></span>

### <span data-ttu-id="825d9-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="825d9-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
HealthProbeMethod : Head
EnabledState      : Enabled
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="825d9-109">注意：HealthProbeMethod 設定不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="825d9-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="825d9-110">建立 PSHealthProbeSetting 物件以用於建立前門</span><span class="sxs-lookup"><span data-stu-id="825d9-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="825d9-111">參數</span><span class="sxs-lookup"><span data-stu-id="825d9-111">PARAMETERS</span></span>

### <span data-ttu-id="825d9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="825d9-112">-DefaultProfile</span></span>
<span data-ttu-id="825d9-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="825d9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="825d9-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="825d9-114">-EnabledState</span></span>
<span data-ttu-id="825d9-115">是否要針對後端多工緩衝處理程式下定義的後端啟用健康狀態查詢。</span><span class="sxs-lookup"><span data-stu-id="825d9-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="825d9-116">只有當啟用單一後端資料庫的單一後端有啟用後端時，才能停用健康狀態查詢。</span><span class="sxs-lookup"><span data-stu-id="825d9-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825d9-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="825d9-117">-HealthProbeMethod</span></span>
<span data-ttu-id="825d9-118">設定要使用哪一種 HTTP 方法來設定後端多工緩衝處理程式下定義的後端。</span><span class="sxs-lookup"><span data-stu-id="825d9-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

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

### <span data-ttu-id="825d9-119">-IntervalIn以秒為單位</span><span class="sxs-lookup"><span data-stu-id="825d9-119">-IntervalInSeconds</span></span>
<span data-ttu-id="825d9-120">健康狀態小數之間的秒數。</span><span class="sxs-lookup"><span data-stu-id="825d9-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="825d9-121">預設值為 30</span><span class="sxs-lookup"><span data-stu-id="825d9-121">Default value is 30</span></span>

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

### <span data-ttu-id="825d9-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="825d9-122">-Name</span></span>
<span data-ttu-id="825d9-123">健康狀態設定名稱。</span><span class="sxs-lookup"><span data-stu-id="825d9-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="825d9-124">-路徑</span><span class="sxs-lookup"><span data-stu-id="825d9-124">-Path</span></span>
<span data-ttu-id="825d9-125">要用於健康狀態探索的路徑。</span><span class="sxs-lookup"><span data-stu-id="825d9-125">The path to use for the health probe.</span></span>
<span data-ttu-id="825d9-126">預設值為 /</span><span class="sxs-lookup"><span data-stu-id="825d9-126">Default is /</span></span>

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

### <span data-ttu-id="825d9-127">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="825d9-127">-Protocol</span></span>
<span data-ttu-id="825d9-128">用於此查詢的通訊協定配置預設值為 HTTP</span><span class="sxs-lookup"><span data-stu-id="825d9-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825d9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="825d9-129">CommonParameters</span></span>
<span data-ttu-id="825d9-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="825d9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="825d9-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="825d9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="825d9-132">輸入</span><span class="sxs-lookup"><span data-stu-id="825d9-132">INPUTS</span></span>

### <span data-ttu-id="825d9-133">沒有</span><span class="sxs-lookup"><span data-stu-id="825d9-133">None</span></span>
## <span data-ttu-id="825d9-134">輸出</span><span class="sxs-lookup"><span data-stu-id="825d9-134">OUTPUTS</span></span>

### <span data-ttu-id="825d9-135">Microsoft.Azure.Commands.FrontDoor.models.PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="825d9-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="825d9-136">筆記</span><span class="sxs-lookup"><span data-stu-id="825d9-136">NOTES</span></span>

## <span data-ttu-id="825d9-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="825d9-137">RELATED LINKS</span></span>

<span data-ttu-id="825d9-138">[New-AzFrontDoor](./New-AzFrontDoor.md) 
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="825d9-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
