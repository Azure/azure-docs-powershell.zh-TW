---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: C5A2A8D2-A840-4712-A8BD-F49C6063D193
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1156b4887e7b97d4e783ec738a939d320fe397a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967738"
---
# <span data-ttu-id="cfdb9-101">Get-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="cfdb9-101">Get-AzureStorSimpleDevice</span></span>

## <span data-ttu-id="cfdb9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cfdb9-102">SYNOPSIS</span></span>
<span data-ttu-id="cfdb9-103">取得附加至資源的裝置。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-103">Gets devices attached to the resource.</span></span>

## <span data-ttu-id="cfdb9-104">句法</span><span class="sxs-lookup"><span data-stu-id="cfdb9-104">SYNTAX</span></span>

### <span data-ttu-id="cfdb9-105">空白 (預設) </span><span class="sxs-lookup"><span data-stu-id="cfdb9-105">Empty (Default)</span></span>
```
Get-AzureStorSimpleDevice [-Type <String>] [-ModelID <String>] [-Detailed] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="cfdb9-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="cfdb9-106">IdentifyById</span></span>
```
Get-AzureStorSimpleDevice [-DeviceId <String>] [-Type <String>] [-ModelID <String>] [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cfdb9-107">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="cfdb9-107">IdentifyByName</span></span>
```
Get-AzureStorSimpleDevice [-DeviceName <String>] [-Type <String>] [-ModelID <String>] [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cfdb9-108">說明</span><span class="sxs-lookup"><span data-stu-id="cfdb9-108">DESCRIPTION</span></span>
<span data-ttu-id="cfdb9-109">**AzureStorSimpleDevice** Cmdlet 會取得附加至資源的 StorSimple 裝置清單。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-109">The **Get-AzureStorSimpleDevice** cmdlet gets a list of StorSimple devices attached to the resource.</span></span>
<span data-ttu-id="cfdb9-110">您可以指定裝置識別碼、名稱、模型識別碼及類型。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-110">You can specify device ID, name, model ID, and type.</span></span>
<span data-ttu-id="cfdb9-111">使用此 Cmdlet 取得的 **DeviceID** 屬性來指定其他 StorSimple Cmdlet 的裝置。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-111">Use the **DeviceID** property obtained by using this cmdlet to specify devices for other StorSimple cmdlets.</span></span>

## <span data-ttu-id="cfdb9-112">示例</span><span class="sxs-lookup"><span data-stu-id="cfdb9-112">EXAMPLES</span></span>

### <span data-ttu-id="cfdb9-113">範例1：在資源上取得可用的裝置</span><span class="sxs-lookup"><span data-stu-id="cfdb9-113">Example 1: Get available devices on a resource</span></span>
```
PS C:\>Get-AzureStorSimpleDevice
DeviceId                  : 6f9ab151-39c7-4ded-b7d0-f5b0968f2766
DeviceName                : 8600-: SHX0881018G88
SerialNumber              : SHX0881018G88
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8600
Status                    : Offline
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8600-shx0991018g00e4-target
TimeZone                  : Pacific Standard Time
ActivationTime            : 2015-04-07T16:32:30.2960842Z
AvailableStorageInBytes   : 535363378479104
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 549755813888000
UsingStorageInBytes       : 12693995520

DeviceId                  : eb30ea31-c856-4cf2-9a02-aee611d6a3b9
DeviceName                : 8100-Delta 001
SerialNumber              : SHX90391XXXXXXX
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8100
Status                    : Online
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8100-shx90193xxxxxxx-target
TimeZone                  : Eastern Standard Time
ActivationTime            : 2015-03-26T14:53:14.4219391Z
AvailableStorageInBytes   : 205509890146304
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 219902325555200
UsingStorageInBytes       : 23904321536

DeviceId                  : edcb0b9b-1ed5-4102-9c5d-c589f7632994
DeviceName                : 8600-Bravo 001
SerialNumber              : SHX0900915G44SY
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8600
Status                    : Online
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8600-shx0900915g44sy-target
TimeZone                  : Eastern Standard Time
ActivationTime            : 2015-03-26T15:36:26.0870525Z
AvailableStorageInBytes   : 535363378479104
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 549755813888000
UsingStorageInBytes       : 978893799424
```

<span data-ttu-id="cfdb9-114">這個命令會取得資源上所有可用的裝置。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-114">This command gets all available devices on a resource.</span></span>
<span data-ttu-id="cfdb9-115">在這個範例中，只有一個裝置可用。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-115">In this example, only one device is available.</span></span>

### <span data-ttu-id="cfdb9-116">範例2：在資源上取得特定的可用裝置</span><span class="sxs-lookup"><span data-stu-id="cfdb9-116">Example 2: Get specific available devices on a resource</span></span>
```
PS C:\>Get-AzureStorSimpleDevice -DeviceName "8600-SHX90193XXXXXXX" -Type Appliance -ModelId "8600"
DeviceId                  : f9db31da-8a6c-4718-8f5b-5ce89e600f28
DeviceName                : 8600-SHX90193XXXXXXX
SerialNumber              : SHX90193XXXXXXX
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8600
Status                    : Online
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8600-shx90193xxxxxxx-target
TimeZone                  : Pacific Standard Time
ActivationTime            : 2015-04-07T18:10:46.4524766Z
AvailableStorageInBytes   : 535363378479104
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 549755813888000
UsingStorageInBytes       : 14445182976
```

<span data-ttu-id="cfdb9-117">這個命令會取得具有指定名稱、類型和模型 ID 之資源上所有可用的裝置。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-117">This command gets all available devices on a resource that have the specified name, type, and model ID.</span></span>

### <span data-ttu-id="cfdb9-118">範例3：取得裝置的詳細資料</span><span class="sxs-lookup"><span data-stu-id="cfdb9-118">Example 3: Get details for a device</span></span>
```
PS C:\>Get-AzureStorSimpleDevice -Name "8600-SHX90193XXXXXXX" -Type Appliance -Detailed
AlertNotification              : Microsoft.WindowsAzure.Management.StorSimple.Models.AlertNotificationSettings
Chap                           : Microsoft.WindowsAzure.Management.StorSimple.Models.ChapSettings
DeviceProperties               : Microsoft.WindowsAzure.Management.StorSimple.Models.DeviceInfo
DnsServer                      : Microsoft.WindowsAzure.Management.StorSimple.Models.DnsServerSettings
InstanceId                     : f9db31da-8a6c-4718-8f5b-5ce89e600f28
Name                           : 
NetInterfaceList               : {Data0, Data1, Data2, Data3...} 
OperationInProgress            : None
RemoteMgmtSettingsInfo         : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteManagementSettings

RemoteMinishellSecretInfo      : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteMinishellSettings
SecretEncryptionCertThumbprint : 
Snapshot                       : Microsoft.WindowsAzure.Management.StorSimple.Models.SnapshotSettings
TimeServer                     : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeSettings
Type                           : Appliance
VirtualApplianceProperties     : Microsoft.WindowsAzure.Management.StorSimple.Models.VirtualApplianceInfo
WebProxy                       : Microsoft.WindowsAzure.Management.StorSimple.Models.WebProxySettings
```

<span data-ttu-id="cfdb9-119">這個命令會取得具有指定名稱和類型之資源的所有可用裝置。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-119">This command gets all available devices on a resource that have the specified name and type.</span></span>
<span data-ttu-id="cfdb9-120">這個命令會指定 *詳細* 的參數。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-120">This command specifies the *Detailed* parameter.</span></span>
<span data-ttu-id="cfdb9-121">此命令會提供它所傳回裝置的其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-121">The command provides additional details about the devices it returns.</span></span>

## <span data-ttu-id="cfdb9-122">參數</span><span class="sxs-lookup"><span data-stu-id="cfdb9-122">PARAMETERS</span></span>

### <span data-ttu-id="cfdb9-123">-詳細資訊</span><span class="sxs-lookup"><span data-stu-id="cfdb9-123">-Detailed</span></span>
<span data-ttu-id="cfdb9-124">表示此 Cmdlet 會傳回它所取得之裝置的裝置詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-124">Indicates that this cmdlet returns device details for the devices that it gets.</span></span>

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

### <span data-ttu-id="cfdb9-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="cfdb9-125">-DeviceId</span></span>
<span data-ttu-id="cfdb9-126">指定要取得之裝置的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-126">Specifies the instance ID of the device to get.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfdb9-127">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="cfdb9-127">-DeviceName</span></span>
<span data-ttu-id="cfdb9-128">指定要取得之 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-128">Specifies the name of the StorSimple device to get.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfdb9-129">-ModelID</span><span class="sxs-lookup"><span data-stu-id="cfdb9-129">-ModelID</span></span>
<span data-ttu-id="cfdb9-130">指定要取得的 StorSimple 裝置型號識別碼。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-130">Specifies the ID of the model of StorSimple devices to get.</span></span>

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

### <span data-ttu-id="cfdb9-131">-設定檔</span><span class="sxs-lookup"><span data-stu-id="cfdb9-131">-Profile</span></span>
<span data-ttu-id="cfdb9-132">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-132">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="cfdb9-133">-類型</span><span class="sxs-lookup"><span data-stu-id="cfdb9-133">-Type</span></span>
<span data-ttu-id="cfdb9-134">指定 StorSimple 裝置的類型。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-134">Specifies the type of a StorSimple device.</span></span>
<span data-ttu-id="cfdb9-135">有效值為： [裝置] 和 [VirtualAppliance]。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-135">Valid values are: Appliance and VirtualAppliance.</span></span>

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

### <span data-ttu-id="cfdb9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfdb9-136">CommonParameters</span></span>
<span data-ttu-id="cfdb9-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfdb9-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfdb9-139">輸入</span><span class="sxs-lookup"><span data-stu-id="cfdb9-139">INPUTS</span></span>

### <span data-ttu-id="cfdb9-140">所有</span><span class="sxs-lookup"><span data-stu-id="cfdb9-140">None</span></span>

## <span data-ttu-id="cfdb9-141">輸出</span><span class="sxs-lookup"><span data-stu-id="cfdb9-141">OUTPUTS</span></span>

### <span data-ttu-id="cfdb9-142">清單 \<DeviceDetails\> 、IEnumerable\<DeviceInfo\></span><span class="sxs-lookup"><span data-stu-id="cfdb9-142">List\<DeviceDetails\>, IEnumerable\<DeviceInfo\></span></span>
<span data-ttu-id="cfdb9-143">如果您指定 *詳細* 的參數，這個 Cmdlet 會傳回 **List \<DeviceDetails\>** 物件。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-143">This cmdlet returns a **List\<DeviceDetails\>** object, if you specify the *Detailed* parameter.</span></span>
<span data-ttu-id="cfdb9-144">如果您沒有指定該參數，則會傳回 **IEnumerable \<DeviceInfo\>** 物件。</span><span class="sxs-lookup"><span data-stu-id="cfdb9-144">If you do not specify that parameter, it returns an **IEnumerable\<DeviceInfo\>** object.</span></span>

## <span data-ttu-id="cfdb9-145">筆記</span><span class="sxs-lookup"><span data-stu-id="cfdb9-145">NOTES</span></span>

## <span data-ttu-id="cfdb9-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="cfdb9-146">RELATED LINKS</span></span>

[<span data-ttu-id="cfdb9-147">AzureStorSimpleResourceCoNtext</span><span class="sxs-lookup"><span data-stu-id="cfdb9-147">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)

[<span data-ttu-id="cfdb9-148">選取-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="cfdb9-148">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


