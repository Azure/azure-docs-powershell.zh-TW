---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 850db31354ebe4a717a5064c7fed56dc94bf1f0d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797146"
---
# <span data-ttu-id="43a6b-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="43a6b-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="43a6b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="43a6b-103">建立用來建立前門的 PSHealthProbeSetting 物件</span><span class="sxs-lookup"><span data-stu-id="43a6b-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="43a6b-104">句法</span><span class="sxs-lookup"><span data-stu-id="43a6b-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43a6b-105">說明</span><span class="sxs-lookup"><span data-stu-id="43a6b-105">DESCRIPTION</span></span>
<span data-ttu-id="43a6b-106">建立用來建立前門的 PSHealthProbeSetting 物件</span><span class="sxs-lookup"><span data-stu-id="43a6b-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="43a6b-107">示例</span><span class="sxs-lookup"><span data-stu-id="43a6b-107">EXAMPLES</span></span>

### <span data-ttu-id="43a6b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="43a6b-108">Example 1</span></span>
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

<span data-ttu-id="43a6b-109">注意： HealthProbeMethod 設定不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="43a6b-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="43a6b-110">建立用來建立前門的 PSHealthProbeSetting 物件</span><span class="sxs-lookup"><span data-stu-id="43a6b-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="43a6b-111">參數</span><span class="sxs-lookup"><span data-stu-id="43a6b-111">PARAMETERS</span></span>

### <span data-ttu-id="43a6b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a6b-112">-DefaultProfile</span></span>
<span data-ttu-id="43a6b-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43a6b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43a6b-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="43a6b-114">-EnabledState</span></span>
<span data-ttu-id="43a6b-115">是否要針對 [backendPools] 下定義的 backends 啟用 health 探測。</span><span class="sxs-lookup"><span data-stu-id="43a6b-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="43a6b-116">只有在單一啟用的後端池中有一個啟用中的後端，才能停用 Health 探測。</span><span class="sxs-lookup"><span data-stu-id="43a6b-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

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

### <span data-ttu-id="43a6b-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="43a6b-117">-HealthProbeMethod</span></span>
<span data-ttu-id="43a6b-118">設定要使用哪個 HTTP 方法來探測在 backendPools 下定義的 backends。</span><span class="sxs-lookup"><span data-stu-id="43a6b-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

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

### <span data-ttu-id="43a6b-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="43a6b-119">-IntervalInSeconds</span></span>
<span data-ttu-id="43a6b-120">Health 探測之間的秒數。</span><span class="sxs-lookup"><span data-stu-id="43a6b-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="43a6b-121">預設值為30</span><span class="sxs-lookup"><span data-stu-id="43a6b-121">Default value is 30</span></span>

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

### <span data-ttu-id="43a6b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="43a6b-122">-Name</span></span>
<span data-ttu-id="43a6b-123">Health 探測設定名稱。</span><span class="sxs-lookup"><span data-stu-id="43a6b-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="43a6b-124">-Path</span><span class="sxs-lookup"><span data-stu-id="43a6b-124">-Path</span></span>
<span data-ttu-id="43a6b-125">要用於 health 探測的路徑。</span><span class="sxs-lookup"><span data-stu-id="43a6b-125">The path to use for the health probe.</span></span>
<span data-ttu-id="43a6b-126">預設值為/</span><span class="sxs-lookup"><span data-stu-id="43a6b-126">Default is /</span></span>

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

### <span data-ttu-id="43a6b-127">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="43a6b-127">-Protocol</span></span>
<span data-ttu-id="43a6b-128">此探針使用的通訊協定配置預設值為 HTTP</span><span class="sxs-lookup"><span data-stu-id="43a6b-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="43a6b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a6b-129">CommonParameters</span></span>
<span data-ttu-id="43a6b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43a6b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a6b-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="43a6b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a6b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="43a6b-132">INPUTS</span></span>

### <span data-ttu-id="43a6b-133">所有</span><span class="sxs-lookup"><span data-stu-id="43a6b-133">None</span></span>
## <span data-ttu-id="43a6b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="43a6b-134">OUTPUTS</span></span>

### <span data-ttu-id="43a6b-135">PSHealthProbeSetting 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="43a6b-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="43a6b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="43a6b-136">NOTES</span></span>

## <span data-ttu-id="43a6b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="43a6b-137">RELATED LINKS</span></span>

<span data-ttu-id="43a6b-138">[新-AzFrontDoor](./New-AzFrontDoor.md) 
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="43a6b-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
