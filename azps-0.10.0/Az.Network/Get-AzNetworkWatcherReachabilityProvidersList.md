---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 805c8d31b075a39fa8ccc407024aa5a32a91fdb6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794385"
---
# <span data-ttu-id="11e7f-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="11e7f-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="11e7f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11e7f-102">SYNOPSIS</span></span>
<span data-ttu-id="11e7f-103">列出指定 Azure 區域所有可用的網際網路服務提供者。</span><span class="sxs-lookup"><span data-stu-id="11e7f-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="11e7f-104">句法</span><span class="sxs-lookup"><span data-stu-id="11e7f-104">SYNTAX</span></span>

### <span data-ttu-id="11e7f-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="11e7f-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11e7f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="11e7f-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11e7f-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="11e7f-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11e7f-108">說明</span><span class="sxs-lookup"><span data-stu-id="11e7f-108">DESCRIPTION</span></span>
<span data-ttu-id="11e7f-109">Get-AzNetworkWatcherReachabilityProvidersList 會列出指定 Azure 區域所有可用的網際網路服務提供者。</span><span class="sxs-lookup"><span data-stu-id="11e7f-109">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="11e7f-110">示例</span><span class="sxs-lookup"><span data-stu-id="11e7f-110">EXAMPLES</span></span>

### <span data-ttu-id="11e7f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="11e7f-111">Example 1</span></span>
```
PS C:\> $nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

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

<span data-ttu-id="11e7f-112">在華盛頓州的 [北京] 中，列出所有在西雅圖、適用于 Azure 資料中心的可用提供者。</span><span class="sxs-lookup"><span data-stu-id="11e7f-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="11e7f-113">參數</span><span class="sxs-lookup"><span data-stu-id="11e7f-113">PARAMETERS</span></span>

### <span data-ttu-id="11e7f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11e7f-114">-AsJob</span></span>
<span data-ttu-id="11e7f-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11e7f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11e7f-116">-城市</span><span class="sxs-lookup"><span data-stu-id="11e7f-116">-City</span></span>
<span data-ttu-id="11e7f-117">城市的名稱。</span><span class="sxs-lookup"><span data-stu-id="11e7f-117">The name of the city.</span></span>

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

### <span data-ttu-id="11e7f-118">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="11e7f-118">-Country</span></span>
<span data-ttu-id="11e7f-119">國家/地區的名稱。</span><span class="sxs-lookup"><span data-stu-id="11e7f-119">The name of the country.</span></span>

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

### <span data-ttu-id="11e7f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e7f-120">-DefaultProfile</span></span>
<span data-ttu-id="11e7f-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="11e7f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11e7f-122">-位置</span><span class="sxs-lookup"><span data-stu-id="11e7f-122">-Location</span></span>
<span data-ttu-id="11e7f-123">要將查詢範圍限定在其中的選用 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="11e7f-123">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="11e7f-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="11e7f-124">-NetworkWatcher</span></span>
<span data-ttu-id="11e7f-125">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="11e7f-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="11e7f-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="11e7f-126">-NetworkWatcherName</span></span>
<span data-ttu-id="11e7f-127">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="11e7f-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="11e7f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11e7f-128">-ResourceGroupName</span></span>
<span data-ttu-id="11e7f-129">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="11e7f-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="11e7f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11e7f-130">-ResourceId</span></span>
<span data-ttu-id="11e7f-131">網路觀察程式資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="11e7f-131">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="11e7f-132">-State</span><span class="sxs-lookup"><span data-stu-id="11e7f-132">-State</span></span>
<span data-ttu-id="11e7f-133">狀態的名稱。</span><span class="sxs-lookup"><span data-stu-id="11e7f-133">The name of the state.</span></span>

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

### <span data-ttu-id="11e7f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e7f-134">CommonParameters</span></span>
<span data-ttu-id="11e7f-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11e7f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e7f-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11e7f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e7f-137">輸入</span><span class="sxs-lookup"><span data-stu-id="11e7f-137">INPUTS</span></span>

### <span data-ttu-id="11e7f-138">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="11e7f-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="11e7f-139">[System.object]。清單 ' 1 [System. 字串，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="11e7f-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="11e7f-140">輸出</span><span class="sxs-lookup"><span data-stu-id="11e7f-140">OUTPUTS</span></span>

### <span data-ttu-id="11e7f-141">PSAvailableProvidersList 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="11e7f-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="11e7f-142">筆記</span><span class="sxs-lookup"><span data-stu-id="11e7f-142">NOTES</span></span>
<span data-ttu-id="11e7f-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，下一步，hop</span><span class="sxs-lookup"><span data-stu-id="11e7f-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="11e7f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="11e7f-144">RELATED LINKS</span></span>

[<span data-ttu-id="11e7f-145">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="11e7f-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="11e7f-146">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="11e7f-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="11e7f-147">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="11e7f-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="11e7f-148">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="11e7f-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="11e7f-149">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="11e7f-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="11e7f-150">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="11e7f-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="11e7f-151">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="11e7f-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="11e7f-152">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="11e7f-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="11e7f-153">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="11e7f-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="11e7f-154">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="11e7f-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="11e7f-155">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="11e7f-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="11e7f-156">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="11e7f-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
