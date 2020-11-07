---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 99D9EFA6-3506-4B0E-ACB5-C6EDBCB5A130
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d73ede26d4bd85a39f4baf2090e581300eafb1b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966961"
---
# <span data-ttu-id="0009a-101">New-AzureStorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="0009a-101">New-AzureStorSimpleNetworkConfig</span></span>

## <span data-ttu-id="0009a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0009a-102">SYNOPSIS</span></span>
<span data-ttu-id="0009a-103">準備網路設定物件。</span><span class="sxs-lookup"><span data-stu-id="0009a-103">Prepares a network configuration object.</span></span>

## <span data-ttu-id="0009a-104">句法</span><span class="sxs-lookup"><span data-stu-id="0009a-104">SYNTAX</span></span>

```
New-AzureStorSimpleNetworkConfig -InterfaceAlias <String> [-EnableIscsi <Boolean>] [-EnableCloud <Boolean>]
 [-Controller0IPv4Address <String>] [-Controller1IPv4Address <String>] [-IPv6Gateway <String>]
 [-IPv4Gateway <String>] [-IPv4Address <String>] [-IPv6Prefix <String>] [-IPv4Netmask <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0009a-105">說明</span><span class="sxs-lookup"><span data-stu-id="0009a-105">DESCRIPTION</span></span>
<span data-ttu-id="0009a-106">**AzureStorSimpleNetworkConfig** Cmdlet 可準備要傳送給 **AzureStorSimpleDevice** Cmdlet 的網路設定物件。</span><span class="sxs-lookup"><span data-stu-id="0009a-106">The **New-AzureStorSimpleNetworkConfig** cmdlet prepares a network configuration object to pass to the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="0009a-107">在 Data0 介面上，只設定 *Controller0IPAddress* 參數和 *Controller1IPAddress* 參數。</span><span class="sxs-lookup"><span data-stu-id="0009a-107">Set the *Controller0IPAddress* parameter and *Controller1IPAddress* parameter only on the Data0 interface.</span></span>
<span data-ttu-id="0009a-108">Data0 僅支援三個設定： *Controller0IPAddress* 、 *Controller1IPAdress* 和 *EnableIscsi* 。</span><span class="sxs-lookup"><span data-stu-id="0009a-108">Data0 supports only three settings: *Controller0IPAddress* , *Controller1IPAdress* , and *EnableIscsi*.</span></span>

## <span data-ttu-id="0009a-109">示例</span><span class="sxs-lookup"><span data-stu-id="0009a-109">EXAMPLES</span></span>

### <span data-ttu-id="0009a-110">範例1：設定 Data0 介面</span><span class="sxs-lookup"><span data-stu-id="0009a-110">Example 1: Configure a Data0 interface</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
VERBOSE: ClientRequestId: 0621d220-a460-48ec-84ec-02a3a82f88b2_PS


IsIscsiEnabled         : True
IsCloudEnabled         : 
Controller0IPv4Address : 10.67.64.48
Controller1IPv4Address : 10.67.64.49
IPv6Gateway            : 
IPv4Gateway            : 
IPv4Address            : 
IPv6Prefix             : 
IPv4Netmask            : 
InterfaceAlias         : Data0

VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
```

<span data-ttu-id="0009a-111">這個命令會建立 Data0 介面的網路設定。</span><span class="sxs-lookup"><span data-stu-id="0009a-111">This command creates network configuration for the Data0 interface.</span></span>
<span data-ttu-id="0009a-112">這個命令會指定 *Controller0IPv4Address* 、 *Controller1IPv4Address* 和 *EnableIscsi* 參數。</span><span class="sxs-lookup"><span data-stu-id="0009a-112">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="0009a-113">這個 Cmdlet 只能設定這三個參數的 Data0。</span><span class="sxs-lookup"><span data-stu-id="0009a-113">This cmdlet can configure Data0 for only these three parameters.</span></span>

### <span data-ttu-id="0009a-114">範例2： Configuren 除 Data0 以外的介面</span><span class="sxs-lookup"><span data-stu-id="0009a-114">Example 2: Configuren an interface other than Data0 an</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data1 -EnableIscsi $True -EnableCloud $True -IPv6Gateway "db8:421e:9a8::a4:1c50" -IPv4Gateway "10.67.64.1" -IPv4Address "10.67.64.48" -IPv6Prefix "2001:db8:a::123/64" -IPv4Netmask "255.255.0.0"
VERBOSE: ClientRequestId: 3a15ff0e-b769-4329-9147-676b1e0acd7d_PS


IsIscsiEnabled         : True
IsCloudEnabled         : True
Controller0IPv4Address : 
Controller1IPv4Address : 
IPv6Gateway            : db8:421e:9a8::a4:1c50
IPv4Gateway            : 10.67.64.1
IPv4Address            : 10.67.64.48
IPv6Prefix             : 2001:db8:a::123/64
IPv4Netmask            : 255.255.0.0
InterfaceAlias         : Data1
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data1
```

<span data-ttu-id="0009a-115">這個命令會設定 Data1 介面。</span><span class="sxs-lookup"><span data-stu-id="0009a-115">This command configures the Data1 interface.</span></span>

### <span data-ttu-id="0009a-116">範例3：修改裝置的設定</span><span class="sxs-lookup"><span data-stu-id="0009a-116">Example 3: Modify a configuration for a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
$OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
$UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : newDeviceName ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device newDeviceName with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="0009a-117">第一個命令會建立 Data0 介面的網路設定。</span><span class="sxs-lookup"><span data-stu-id="0009a-117">The first command creates a network configuration for the Data0 interface.</span></span>
<span data-ttu-id="0009a-118">這個命令會指定 *Controller0IPv4Address* 、 *Controller1IPv4Address* 和 *EnableIscsi* 參數。</span><span class="sxs-lookup"><span data-stu-id="0009a-118">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="0009a-119">該命令會將結果儲存在 $NetworkConfigData 0 變數中。</span><span class="sxs-lookup"><span data-stu-id="0009a-119">The command stores the result in the $NetworkConfigData0 variable.</span></span>

<span data-ttu-id="0009a-120">第二個命令使用 **AzureStorSimpleDevice** Cmdlet 和 **Where 物件** 核心 Cmdlet 來取得線上 StorSimple 裝置，然後將它儲存在 $OnlineDevice 變數中。</span><span class="sxs-lookup"><span data-stu-id="0009a-120">The second command uses the **Get-AzureStorSimpleDevice** cmdlet and the **Where-Object** core cmdlet to get an online StorSimple device, and then stores it in the $OnlineDevice variable.</span></span>

<span data-ttu-id="0009a-121">最後一個命令會使用 AzureStorSimpleDevice Cmdlet 來修改具有指定裝置識別碼之裝置的 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="0009a-121">The final command modifies the configuration for the device that has the specified device ID by using the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="0009a-122">此命令會使用在第一個命令中建立的目前 Cmdlet 的 configuration 物件。</span><span class="sxs-lookup"><span data-stu-id="0009a-122">The command uses the configuration object that the current cmdlet created in the first command.</span></span>

## <span data-ttu-id="0009a-123">參數</span><span class="sxs-lookup"><span data-stu-id="0009a-123">PARAMETERS</span></span>

### <span data-ttu-id="0009a-124">-Controller0IPv4Address</span><span class="sxs-lookup"><span data-stu-id="0009a-124">-Controller0IPv4Address</span></span>
<span data-ttu-id="0009a-125">指定控制器0的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="0009a-125">Specifies the IPv4 address for controller 0.</span></span>
<span data-ttu-id="0009a-126">請僅為 Data0 介面指定此參數。</span><span class="sxs-lookup"><span data-stu-id="0009a-126">Specify this parameter only for the Data0 interface.</span></span>

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

### <span data-ttu-id="0009a-127">-Controller1IPv4Address</span><span class="sxs-lookup"><span data-stu-id="0009a-127">-Controller1IPv4Address</span></span>
<span data-ttu-id="0009a-128">指定控制器1的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="0009a-128">Specifies the IPv4 address for controller 1.</span></span>
<span data-ttu-id="0009a-129">請僅為 Data0 介面指定此參數。</span><span class="sxs-lookup"><span data-stu-id="0009a-129">Specify this parameter only for the Data0 interface.</span></span>

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

### <span data-ttu-id="0009a-130">-EnableCloud</span><span class="sxs-lookup"><span data-stu-id="0009a-130">-EnableCloud</span></span>
<span data-ttu-id="0009a-131">指出是否要雲端啟用介面。</span><span class="sxs-lookup"><span data-stu-id="0009a-131">Indicates whether to cloud-enable the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0009a-132">-EnableIscsi</span><span class="sxs-lookup"><span data-stu-id="0009a-132">-EnableIscsi</span></span>
<span data-ttu-id="0009a-133">指出是否要針對介面啟用網際網路 SCSI (ISCSI) 。</span><span class="sxs-lookup"><span data-stu-id="0009a-133">Indicates whether to enable Internet SCSI (ISCSI) for the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0009a-134">-InterfaceAlias</span><span class="sxs-lookup"><span data-stu-id="0009a-134">-InterfaceAlias</span></span>
<span data-ttu-id="0009a-135">指定此 Cmdlet 提供其設定之介面的介面別名。</span><span class="sxs-lookup"><span data-stu-id="0009a-135">Specifies the interface alias of interface for which this cmdlet supplies settings.</span></span>
<span data-ttu-id="0009a-136">有效的值是從 Data0 到 Data5。</span><span class="sxs-lookup"><span data-stu-id="0009a-136">Valid values are from Data0 to Data5.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0009a-137">-IPv4Address</span><span class="sxs-lookup"><span data-stu-id="0009a-137">-IPv4Address</span></span>
<span data-ttu-id="0009a-138">指定介面的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="0009a-138">Specifies the IPv4 address for the interface.</span></span>

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

### <span data-ttu-id="0009a-139">-IPv4Gateway</span><span class="sxs-lookup"><span data-stu-id="0009a-139">-IPv4Gateway</span></span>
<span data-ttu-id="0009a-140">指定閘道的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="0009a-140">Specifies the IPv4 address of a gateway.</span></span>

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

### <span data-ttu-id="0009a-141">-IPv4Netmask</span><span class="sxs-lookup"><span data-stu-id="0009a-141">-IPv4Netmask</span></span>
<span data-ttu-id="0009a-142">指定介面的 IPv4 網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="0009a-142">Specifies the IPv4 netmask for the interface.</span></span>

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

### <span data-ttu-id="0009a-143">-IPv6Gateway</span><span class="sxs-lookup"><span data-stu-id="0009a-143">-IPv6Gateway</span></span>
<span data-ttu-id="0009a-144">指定介面的 IPv6 閘道。</span><span class="sxs-lookup"><span data-stu-id="0009a-144">Specifies the IPv6 gateway for the interface.</span></span>

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

### <span data-ttu-id="0009a-145">-IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="0009a-145">-IPv6Prefix</span></span>
<span data-ttu-id="0009a-146">指定介面的 IPv6 前置詞。</span><span class="sxs-lookup"><span data-stu-id="0009a-146">Specifies the IPv6 prefix for the interface.</span></span>

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

### <span data-ttu-id="0009a-147">-設定檔</span><span class="sxs-lookup"><span data-stu-id="0009a-147">-Profile</span></span>
<span data-ttu-id="0009a-148">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0009a-148">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0009a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0009a-149">CommonParameters</span></span>
<span data-ttu-id="0009a-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0009a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0009a-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0009a-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0009a-152">輸入</span><span class="sxs-lookup"><span data-stu-id="0009a-152">INPUTS</span></span>

### <span data-ttu-id="0009a-153">所有</span><span class="sxs-lookup"><span data-stu-id="0009a-153">None</span></span>

## <span data-ttu-id="0009a-154">輸出</span><span class="sxs-lookup"><span data-stu-id="0009a-154">OUTPUTS</span></span>

### <span data-ttu-id="0009a-155">NetworkConfig</span><span class="sxs-lookup"><span data-stu-id="0009a-155">NetworkConfig</span></span>
<span data-ttu-id="0009a-156">這個 Cmdlet 會傳回包含下列屬性的 NetworkConfig 物件：</span><span class="sxs-lookup"><span data-stu-id="0009a-156">This cmdlet returns a NetworkConfig object that contains the following properties:</span></span> 

- <span data-ttu-id="0009a-157">**IsIscsiEnabled** ( **布林值** ) </span><span class="sxs-lookup"><span data-stu-id="0009a-157">**IsIscsiEnabled** ( **Boolean** )</span></span> 
- <span data-ttu-id="0009a-158">**IsCloudEnabled** ( **布林值** ) </span><span class="sxs-lookup"><span data-stu-id="0009a-158">**IsCloudEnabled** ( **Boolean** )</span></span>
- <span data-ttu-id="0009a-159">**Controller0IPv4Address** ( **IPAddress** ) </span><span class="sxs-lookup"><span data-stu-id="0009a-159">**Controller0IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="0009a-160">**Controller1IPv4Address** ( **IPAddress** ) </span><span class="sxs-lookup"><span data-stu-id="0009a-160">**Controller1IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="0009a-161">**IPv6Gateway** ( **IPAddress** ) </span><span class="sxs-lookup"><span data-stu-id="0009a-161">**IPv6Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="0009a-162">**IPv4Gateway** ( **IPAddress** ) </span><span class="sxs-lookup"><span data-stu-id="0009a-162">**IPv4Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="0009a-163">**IPv4Address** ( **IPAddress** ) </span><span class="sxs-lookup"><span data-stu-id="0009a-163">**IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="0009a-164">**IPv6Prefix** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="0009a-164">**IPv6Prefix** ( **String** )</span></span>
- <span data-ttu-id="0009a-165">**IPv4Netmask** ( **IPAddress** ) </span><span class="sxs-lookup"><span data-stu-id="0009a-165">**IPv4Netmask** ( **IPAddress** )</span></span> 
- <span data-ttu-id="0009a-166">**InterfaceAlias** ( **NetInterfaceId** ) </span><span class="sxs-lookup"><span data-stu-id="0009a-166">**InterfaceAlias** ( **NetInterfaceId** )</span></span>

## <span data-ttu-id="0009a-167">筆記</span><span class="sxs-lookup"><span data-stu-id="0009a-167">NOTES</span></span>

## <span data-ttu-id="0009a-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="0009a-168">RELATED LINKS</span></span>

[<span data-ttu-id="0009a-169">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="0009a-169">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)

[<span data-ttu-id="0009a-170">AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="0009a-170">Get-AzureStorSimpleDevice</span></span>](./Get-AzureStorSimpleDevice.md)


