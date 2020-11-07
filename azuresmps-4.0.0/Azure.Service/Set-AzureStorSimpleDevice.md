---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: AE8E6778-1299-4EC7-BFE0-3FB464AA7BB4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7bea5cbf2b5e10c85aaafa43203c207193040464
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967199"
---
# <span data-ttu-id="75cf7-101">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="75cf7-101">Set-AzureStorSimpleDevice</span></span>

## <span data-ttu-id="75cf7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="75cf7-103">變更裝置的裝置設定。</span><span class="sxs-lookup"><span data-stu-id="75cf7-103">Changes the device configuration for a device.</span></span>

## <span data-ttu-id="75cf7-104">句法</span><span class="sxs-lookup"><span data-stu-id="75cf7-104">SYNTAX</span></span>

### <span data-ttu-id="75cf7-105">IdentifyByName (預設) </span><span class="sxs-lookup"><span data-stu-id="75cf7-105">IdentifyByName (Default)</span></span>
```
Set-AzureStorSimpleDevice -DeviceName <String> [-NewName <String>] [-TimeZone <TimeZoneInfo>]
 [-SecondaryDnsServer <String>] [-StorSimpleNetworkConfig <NetworkConfig[]>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="75cf7-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="75cf7-106">IdentifyById</span></span>
```
Set-AzureStorSimpleDevice -DeviceId <String> [-NewName <String>] [-TimeZone <TimeZoneInfo>]
 [-SecondaryDnsServer <String>] [-StorSimpleNetworkConfig <NetworkConfig[]>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="75cf7-107">說明</span><span class="sxs-lookup"><span data-stu-id="75cf7-107">DESCRIPTION</span></span>
<span data-ttu-id="75cf7-108">**AzureStorSimpleDevice** Cmdlet 會變更裝置的裝置配置。</span><span class="sxs-lookup"><span data-stu-id="75cf7-108">The **Set-AzureStorSimpleDevice** cmdlet changes the device configuration for a device.</span></span>
<span data-ttu-id="75cf7-109">如果您是第一次設定裝置，您必須指定 [ *時區* ]、[ *SecondaryDnsServer* ] 和 [ *StorSimpleNetworkConfig* ] 參數。</span><span class="sxs-lookup"><span data-stu-id="75cf7-109">If you are setting up a device for the first time, you must specify the *TimeZone* , *SecondaryDnsServer* , and *StorSimpleNetworkConfig* parameters.</span></span>
<span data-ttu-id="75cf7-110">您必須加入 Data0 的網路設定與 controller0 和 controller1 和 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="75cf7-110">You must include network configuration for Data0 with controller0 and controller1 and IP addresses.</span></span>
<span data-ttu-id="75cf7-111">您必須有至少一個網際網路 SCSI (ISCSI) 的網路介面，才能第一次設定裝置。</span><span class="sxs-lookup"><span data-stu-id="75cf7-111">There must be at least one Internet SCSI (ISCSI)-enabled network interface to configure the device for the first time.</span></span>

## <span data-ttu-id="75cf7-112">示例</span><span class="sxs-lookup"><span data-stu-id="75cf7-112">EXAMPLES</span></span>

### <span data-ttu-id="75cf7-113">範例1：修改裝置的設定</span><span class="sxs-lookup"><span data-stu-id="75cf7-113">Example 1: Modify the configuration for a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" 
PS C:\> $TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -TimeZone $TimeZoneInfo -SecondaryDnsServer 10.8.8.8 -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="75cf7-114">第一個命令會建立 Data0 介面的網路設定。</span><span class="sxs-lookup"><span data-stu-id="75cf7-114">The first command creates a network configuration for the Data0 interface.</span></span>
<span data-ttu-id="75cf7-115">這個命令會指定 *Controller0IPv4Address* 、 *Controller1IPv4Address* 和 *EnableIscsi* 參數。</span><span class="sxs-lookup"><span data-stu-id="75cf7-115">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="75cf7-116">該命令會將結果儲存在 $NetworkConfigData 0 變數中。</span><span class="sxs-lookup"><span data-stu-id="75cf7-116">The command stores the result in the $NetworkConfigData0 variable.</span></span>

<span data-ttu-id="75cf7-117">第二個命令使用 **TimeZoneInfo** .net 類別和標準語法來取得太平洋標準時區，並將該物件儲存在 $TimeZoneInfo 變數中。</span><span class="sxs-lookup"><span data-stu-id="75cf7-117">The second command uses the **System.TimeZoneInfo** .NET class and standard syntax to get Pacific Standard Time zone, and stores that object in the $TimeZoneInfo variable.</span></span>

<span data-ttu-id="75cf7-118">第三個命令使用 **AzureStorSimpleDevice** Cmdlet 和 **Where 物件** 核心 Cmdlet 來取得線上 StorSimple 裝置，然後將它儲存在 $OnlineDevice 變數中。</span><span class="sxs-lookup"><span data-stu-id="75cf7-118">The third command uses the **Get-AzureStorSimpleDevice** cmdlet and the **Where-Object** core cmdlet to get an online StorSimple device, and then stores it in the $OnlineDevice variable.</span></span>

<span data-ttu-id="75cf7-119">最後一個命令會修改具有指定裝置識別碼之裝置的設定。</span><span class="sxs-lookup"><span data-stu-id="75cf7-119">The final command modifies the configuration for the device that has the specified device ID.</span></span>
<span data-ttu-id="75cf7-120">此命令會使用在第一個命令中建立的目前 Cmdlet 的 configuration 物件。</span><span class="sxs-lookup"><span data-stu-id="75cf7-120">The command uses the configuration object that the current cmdlet created in the first command.</span></span>
<span data-ttu-id="75cf7-121">該命令會使用儲存在 $TimeZoneInfo 中的時區。</span><span class="sxs-lookup"><span data-stu-id="75cf7-121">The command uses the time zone stored in $TimeZoneInfo.</span></span>

### <span data-ttu-id="75cf7-122">範例2：將設定物件輸送至修改裝置</span><span class="sxs-lookup"><span data-stu-id="75cf7-122">Example 2: Pipe the configuration object to modify a device</span></span>
```
PS C:\>$TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" | Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -TimeZone $TimeZoneInfo -SecondaryDnsServer 10.8.8.8 
VERBOSE: ClientRequestId: fa2f5000-169c-4feb-abbf-23f4b5c837fa_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: fae6a491-919c-44b2-93e0-0c51f202c24b_PS
VERBOSE: ClientRequestId: e1803427-a097-4d58-ab7d-14a4c39fd768_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 9e796c3d-3100-46ab-9a09-0e10c73a296f_PS
VERBOSE: ClientRequestId: 5b4cad96-31f4-4d07-a278-df5af3e06ad4_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: 9061f7df-144f-4f30-858c-045d882ca392_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 2ed2fa9b-8459-4cd6-9a61-5fc25ced2815_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="75cf7-123">這個範例與第一個範例的配置更新相同，但最終命令會使用管線運算子將網路設定物件傳到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="75cf7-123">This example does the same configuration update as the first example, except that the final command passes the network configuration object to the current cmdlet by using the pipeline operator.</span></span>

### <span data-ttu-id="75cf7-124">範例3：將時區物件輸送至修改裝置</span><span class="sxs-lookup"><span data-stu-id="75cf7-124">Example 3: Pipe the time zone object to modify a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" 
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" } | Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -SecondaryDnsServer 10.8.8.8 -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: cfc3f3c7-a8b6-462b-96f4-124050b736fe_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 6017b76f-a771-4bf8-901e-14876e0f9962_PS
VERBOSE: ClientRequestId: 59a9275c-9005-4e8a-b68b-efa1e6c27d47_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 08e5142a-b038-4607-8690-0c5a8b948352_PS
VERBOSE: ClientRequestId: 218af244-b8f4-4a4b-817e-8f67e1323f03_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: fbd1f32d-1d74-432e-9dc0-90b46674884a_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 981cb941-252c-4898-ba9f-f19e5b8bcaa4_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="75cf7-125">這個範例與第一個範例的配置更新相同，但最終命令會使用管線運算子將時區物件傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="75cf7-125">This example does the same configuration update as the first example, except that the final command passes the time zone object to the current cmdlet by using the pipeline operator.</span></span>

## <span data-ttu-id="75cf7-126">參數</span><span class="sxs-lookup"><span data-stu-id="75cf7-126">PARAMETERS</span></span>

### <span data-ttu-id="75cf7-127">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="75cf7-127">-DeviceId</span></span>
<span data-ttu-id="75cf7-128">指定要設定之 StorSimple 裝置的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="75cf7-128">Specifies the instance ID of the StorSimple device to configure.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cf7-129">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="75cf7-129">-DeviceName</span></span>
<span data-ttu-id="75cf7-130">指定要設定的 StorSimple 裝置易記名稱。</span><span class="sxs-lookup"><span data-stu-id="75cf7-130">Specifies the friendly name of the StorSimple device to configure.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75cf7-131">-NewName</span><span class="sxs-lookup"><span data-stu-id="75cf7-131">-NewName</span></span>
<span data-ttu-id="75cf7-132">指定 StorSimple 裝置的新易記名稱。</span><span class="sxs-lookup"><span data-stu-id="75cf7-132">Specifies the new friendly name of the StorSimple device.</span></span>

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

### <span data-ttu-id="75cf7-133">-設定檔</span><span class="sxs-lookup"><span data-stu-id="75cf7-133">-Profile</span></span>
<span data-ttu-id="75cf7-134">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="75cf7-134">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="75cf7-135">-SecondaryDnsServer</span><span class="sxs-lookup"><span data-stu-id="75cf7-135">-SecondaryDnsServer</span></span>
<span data-ttu-id="75cf7-136">指定 StorSimple 裝置的副 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="75cf7-136">Specifies a secondary DNS server for the StorSimple device.</span></span>

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

### <span data-ttu-id="75cf7-137">-StorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="75cf7-137">-StorSimpleNetworkConfig</span></span>
<span data-ttu-id="75cf7-138">指定裝置上介面的網路設定 objectss 陣列。</span><span class="sxs-lookup"><span data-stu-id="75cf7-138">Specifies an array of network configuration objectss for interfaces on a device.</span></span>
<span data-ttu-id="75cf7-139">若要取得 **NetworkConfig** 物件，請使用 New-AzureStorSimpleNetworkConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="75cf7-139">To obtain a **NetworkConfig** object, use the New-AzureStorSimpleNetworkConfig cmdlet.</span></span>

```yaml
Type: NetworkConfig[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75cf7-140">-時區</span><span class="sxs-lookup"><span data-stu-id="75cf7-140">-TimeZone</span></span>
<span data-ttu-id="75cf7-141">指定裝置的時區。</span><span class="sxs-lookup"><span data-stu-id="75cf7-141">Specifies a time zone for the device.</span></span>
<span data-ttu-id="75cf7-142">您可以使用 **GetSystemTimeZone ( # B1** 方法來建立 **TimeZoneInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="75cf7-142">You can create a **TimeZoneInfo** object by using the **GetSystemTimeZone()** method.</span></span>
<span data-ttu-id="75cf7-143">例如，這個命令會針對太平洋標準時間建立時區資訊物件： `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span><span class="sxs-lookup"><span data-stu-id="75cf7-143">For example, this command creates a time zone information object for Pacific Standard Time: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span></span>

```yaml
Type: TimeZoneInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75cf7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75cf7-144">CommonParameters</span></span>
<span data-ttu-id="75cf7-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75cf7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75cf7-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="75cf7-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75cf7-147">輸入</span><span class="sxs-lookup"><span data-stu-id="75cf7-147">INPUTS</span></span>

### <span data-ttu-id="75cf7-148">NetworkConfig, TimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="75cf7-148">NetworkConfig, TimeZoneInfo</span></span>
<span data-ttu-id="75cf7-149">您可以將 **NetworkConfig** 物件或 **TimeZoneInfo** 輸送至此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="75cf7-149">You can pipe a **NetworkConfig** object or a **TimeZoneInfo** to this cmdlet.</span></span>

## <span data-ttu-id="75cf7-150">輸出</span><span class="sxs-lookup"><span data-stu-id="75cf7-150">OUTPUTS</span></span>

### <span data-ttu-id="75cf7-151">DeviceDetails</span><span class="sxs-lookup"><span data-stu-id="75cf7-151">DeviceDetails</span></span>
<span data-ttu-id="75cf7-152">這個 Cmdlet 會傳回虛擬裝置的更新裝置詳細資料。</span><span class="sxs-lookup"><span data-stu-id="75cf7-152">This cmdlet returns updated device details for the virtual device.</span></span>

## <span data-ttu-id="75cf7-153">筆記</span><span class="sxs-lookup"><span data-stu-id="75cf7-153">NOTES</span></span>

## <span data-ttu-id="75cf7-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="75cf7-154">RELATED LINKS</span></span>

[<span data-ttu-id="75cf7-155">新-AzureStorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="75cf7-155">New-AzureStorSimpleNetworkConfig</span></span>](./New-AzureStorSimpleNetworkConfig.md)

[<span data-ttu-id="75cf7-156">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="75cf7-156">Set-AzureStorSimpleVirtualDevice</span></span>](./Set-AzureStorSimpleVirtualDevice.md)


