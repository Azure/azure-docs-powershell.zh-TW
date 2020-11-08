---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 88cbb5417e8a82ede25cc77274294a5dc4f64b9c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126331"
---
# <span data-ttu-id="19510-101">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="19510-101">Stop-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="19510-102">摘要</span><span class="sxs-lookup"><span data-stu-id="19510-102">SYNOPSIS</span></span>
<span data-ttu-id="19510-103">停止 Vpn 連線的 [資料包捕獲] 作業</span><span class="sxs-lookup"><span data-stu-id="19510-103">Stops Packet Capture Operation on a Vpn connection</span></span>

## <span data-ttu-id="19510-104">句法</span><span class="sxs-lookup"><span data-stu-id="19510-104">SYNTAX</span></span>

### <span data-ttu-id="19510-105">ByVpnConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="19510-105">ByVpnConnectionName (Default)</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-LinkConnectionName <String>] -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19510-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="19510-106">ByVpnConnectionObject</span></span>
```
Stop-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-LinkConnectionName <String>]
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19510-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="19510-107">ByVpnConnectionResourceId</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceId <String> [-LinkConnectionName <String>] -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19510-108">說明</span><span class="sxs-lookup"><span data-stu-id="19510-108">DESCRIPTION</span></span>
<span data-ttu-id="19510-109">在 Vpn 連線時停止 [資料包捕獲] 作業，並將在指定 SasUrl 的儲存空間容器中上傳結果。</span><span class="sxs-lookup"><span data-stu-id="19510-109">Stops Packet Capture Operation on a Vpn connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="19510-110">示例</span><span class="sxs-lookup"><span data-stu-id="19510-110">EXAMPLES</span></span>

### <span data-ttu-id="19510-111">範例1</span><span class="sxs-lookup"><span data-stu-id="19510-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVpnConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -ParentResourceName "VpnGw1" -LinkConnectionName "SiteLink1,SiteLink2" -SasUrl $sasurl
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

### <span data-ttu-id="19510-112">範例2</span><span class="sxs-lookup"><span data-stu-id="19510-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVpnConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVpnConnectionPacketCapture -InputObject $conn -SasUrl $sasurl -LinkConnectionName "SiteLink1,SiteLink2"
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

## <span data-ttu-id="19510-113">參數</span><span class="sxs-lookup"><span data-stu-id="19510-113">PARAMETERS</span></span>

### <span data-ttu-id="19510-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19510-114">-AsJob</span></span>
<span data-ttu-id="19510-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="19510-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19510-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19510-116">-DefaultProfile</span></span>
<span data-ttu-id="19510-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="19510-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19510-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19510-118">-InputObject</span></span>
<span data-ttu-id="19510-119">要開始建立資料包捕獲的 Vpn 連線物件。</span><span class="sxs-lookup"><span data-stu-id="19510-119">The Vpn connection object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19510-120">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="19510-120">-LinkConnectionName</span></span>
<span data-ttu-id="19510-121">SiteLinkConnection 的名稱。</span><span class="sxs-lookup"><span data-stu-id="19510-121">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="19510-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="19510-122">-Name</span></span>
<span data-ttu-id="19510-123">要開始建立資料包捕獲的 Vpn 連線名稱。</span><span class="sxs-lookup"><span data-stu-id="19510-123">The Vpn connection name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19510-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="19510-124">-ParentResourceName</span></span>
<span data-ttu-id="19510-125">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="19510-125">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19510-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19510-126">-ResourceGroupName</span></span>
<span data-ttu-id="19510-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="19510-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19510-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19510-128">-ResourceId</span></span>
<span data-ttu-id="19510-129">要開始進行資料包捕獲之 VpnConnection 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="19510-129">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19510-130">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="19510-130">-SasUrl</span></span>
<span data-ttu-id="19510-131">在 Vpn 上停止資料包捕獲的 SAS Url。</span><span class="sxs-lookup"><span data-stu-id="19510-131">SAS Url for stop packet capture on Vpn.</span></span>

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

### <span data-ttu-id="19510-132">-確認</span><span class="sxs-lookup"><span data-stu-id="19510-132">-Confirm</span></span>
<span data-ttu-id="19510-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="19510-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19510-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19510-134">-WhatIf</span></span>
<span data-ttu-id="19510-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="19510-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19510-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="19510-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19510-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19510-137">CommonParameters</span></span>
<span data-ttu-id="19510-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="19510-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19510-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="19510-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19510-140">輸入</span><span class="sxs-lookup"><span data-stu-id="19510-140">INPUTS</span></span>

### <span data-ttu-id="19510-141">PSVpnConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="19510-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="19510-142">System.object</span><span class="sxs-lookup"><span data-stu-id="19510-142">System.String</span></span>

## <span data-ttu-id="19510-143">輸出</span><span class="sxs-lookup"><span data-stu-id="19510-143">OUTPUTS</span></span>

### <span data-ttu-id="19510-144">PSVpnPacketCaptureResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="19510-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span></span>

## <span data-ttu-id="19510-145">筆記</span><span class="sxs-lookup"><span data-stu-id="19510-145">NOTES</span></span>

## <span data-ttu-id="19510-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="19510-146">RELATED LINKS</span></span>

[<span data-ttu-id="19510-147">開始-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="19510-147">Start-AzVpnConnectionPacketCapture</span></span>](./Start-AzVpnConnectionPacketCapture.md)