---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityproviderslist
schema: 2.0.0
ms.openlocfilehash: c5a681f8be210e76ecbf3bc965e7e9e9c108a94a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800105"
---
# <span data-ttu-id="d59b1-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d59b1-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="d59b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d59b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d59b1-103">列出指定 Azure 區域所有可用的網際網路服務提供者。</span><span class="sxs-lookup"><span data-stu-id="d59b1-103">Lists all available internet service providers for a specified Azure region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d59b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="d59b1-104">SYNTAX</span></span>

### <span data-ttu-id="d59b1-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="d59b1-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d59b1-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d59b1-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d59b1-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d59b1-107">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d59b1-108">說明</span><span class="sxs-lookup"><span data-stu-id="d59b1-108">DESCRIPTION</span></span>
<span data-ttu-id="d59b1-109">Get-AzureRmNetworkWatcherReachabilityProvidersList 會列出指定 Azure 區域所有可用的網際網路服務提供者。</span><span class="sxs-lookup"><span data-stu-id="d59b1-109">The Get-AzureRmNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="d59b1-110">示例</span><span class="sxs-lookup"><span data-stu-id="d59b1-110">EXAMPLES</span></span>

### <span data-ttu-id="d59b1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d59b1-111">Example 1</span></span>
```
PS C:\> $nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

"countries" : [
    {
        "countryName" : "United States",
        "states" : [
            {
                "stateName" : "washington",
                "cities" : [
                    {
                        "cityName" : "seattle",
                        "providers" : [
                            "Comcast Cable Communications, Inc. - ASN 7922",
                            "Comcast Cable Communications, LLC - ASN 7922",
                            "Level 3 Communications, Inc. (GBLX) - ASN 3549",
                            "Qwest Communications Company, LLC - ASN 209"
                        ]
                    }
                ]
            }
        ]
    }
]
```

<span data-ttu-id="d59b1-112">在華盛頓州的 [北京] 中，列出所有在西雅圖、適用于 Azure 資料中心的可用提供者。</span><span class="sxs-lookup"><span data-stu-id="d59b1-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="d59b1-113">參數</span><span class="sxs-lookup"><span data-stu-id="d59b1-113">PARAMETERS</span></span>

### <span data-ttu-id="d59b1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d59b1-114">-AsJob</span></span>
<span data-ttu-id="d59b1-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d59b1-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59b1-116">-城市</span><span class="sxs-lookup"><span data-stu-id="d59b1-116">-City</span></span>
<span data-ttu-id="d59b1-117">城市的名稱。</span><span class="sxs-lookup"><span data-stu-id="d59b1-117">The name of the city.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59b1-118">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="d59b1-118">-Country</span></span>
<span data-ttu-id="d59b1-119">國家/地區的名稱。</span><span class="sxs-lookup"><span data-stu-id="d59b1-119">The name of the country.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59b1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d59b1-120">-DefaultProfile</span></span>
<span data-ttu-id="d59b1-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d59b1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59b1-122">-位置</span><span class="sxs-lookup"><span data-stu-id="d59b1-122">-Location</span></span>
<span data-ttu-id="d59b1-123">要將查詢範圍限定在其中的選用 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="d59b1-123">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59b1-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d59b1-124">-NetworkWatcher</span></span>
<span data-ttu-id="d59b1-125">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="d59b1-125">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d59b1-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d59b1-126">-NetworkWatcherName</span></span>
<span data-ttu-id="d59b1-127">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="d59b1-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59b1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d59b1-128">-ResourceGroupName</span></span>
<span data-ttu-id="d59b1-129">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d59b1-129">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59b1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d59b1-130">-ResourceId</span></span>
<span data-ttu-id="d59b1-131">網路觀察程式資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d59b1-131">The Id of network watcher resource.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d59b1-132">-State</span><span class="sxs-lookup"><span data-stu-id="d59b1-132">-State</span></span>
<span data-ttu-id="d59b1-133">狀態的名稱。</span><span class="sxs-lookup"><span data-stu-id="d59b1-133">The name of the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59b1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d59b1-134">CommonParameters</span></span>
<span data-ttu-id="d59b1-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d59b1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d59b1-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d59b1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d59b1-137">輸入</span><span class="sxs-lookup"><span data-stu-id="d59b1-137">INPUTS</span></span>

### <span data-ttu-id="d59b1-138">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d59b1-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d59b1-139">[System.object]。清單 ' 1 [System. 字串，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d59b1-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d59b1-140">輸出</span><span class="sxs-lookup"><span data-stu-id="d59b1-140">OUTPUTS</span></span>

### <span data-ttu-id="d59b1-141">PSAvailableProvidersList 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d59b1-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="d59b1-142">筆記</span><span class="sxs-lookup"><span data-stu-id="d59b1-142">NOTES</span></span>
<span data-ttu-id="d59b1-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，下一步，hop</span><span class="sxs-lookup"><span data-stu-id="d59b1-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="d59b1-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="d59b1-144">RELATED LINKS</span></span>

[<span data-ttu-id="d59b1-145">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d59b1-145">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d59b1-146">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d59b1-146">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d59b1-147">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d59b1-147">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d59b1-148">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d59b1-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="d59b1-149">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d59b1-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d59b1-150">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d59b1-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="d59b1-151">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d59b1-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d59b1-152">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d59b1-152">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d59b1-153">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d59b1-153">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="d59b1-154">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d59b1-154">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d59b1-155">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d59b1-155">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d59b1-156">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d59b1-156">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
