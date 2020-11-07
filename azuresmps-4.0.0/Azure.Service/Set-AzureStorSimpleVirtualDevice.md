---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CE1C6576-234E-4891-9158-FA45B64B786C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41e8641b01dcb95a6b6939ff3551fe03b642ddf0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966881"
---
# <span data-ttu-id="131b6-101">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="131b6-101">Set-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="131b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="131b6-102">SYNOPSIS</span></span>
<span data-ttu-id="131b6-103">建立或更新 StorSimple 虛擬裝置的裝置設定。</span><span class="sxs-lookup"><span data-stu-id="131b6-103">Creates or updates the device configuration of a StorSimple virtual device.</span></span>

## <span data-ttu-id="131b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="131b6-104">SYNTAX</span></span>

```
Set-AzureStorSimpleVirtualDevice -DeviceName <String> -SecretKey <String> -AdministratorPassword <String>
 -SnapshotManagerPassword <String> [-TimeZone <TimeZoneInfo>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="131b6-105">說明</span><span class="sxs-lookup"><span data-stu-id="131b6-105">DESCRIPTION</span></span>
<span data-ttu-id="131b6-106">**AzureStorSimpleVirtualDevice** Cmdlet 會建立或更新 Azure StorSimple 虛擬裝置的裝置設定。</span><span class="sxs-lookup"><span data-stu-id="131b6-106">The **Set-AzureStorSimpleVirtualDevice** cmdlet creates or updates the device configuration of an Azure StorSimple virtual device.</span></span>

## <span data-ttu-id="131b6-107">示例</span><span class="sxs-lookup"><span data-stu-id="131b6-107">EXAMPLES</span></span>

### <span data-ttu-id="131b6-108">範例1：更新虛擬裝置</span><span class="sxs-lookup"><span data-stu-id="131b6-108">Example 1: Update a virtual device</span></span>
```
PS C:\>$TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ==" -TimeZone $TimeZoneInfo
VERBOSE: ClientRequestId: e31f0d6b-451d-4c1d-b2f1-3fc84c13972c_PS
VERBOSE: ClientRequestId: df58db83-d563-4a2e-bbb4-9576f0e69ca6_PS
VERBOSE: ClientRequestId: 494a9f0d-79ee-4fde-ab4d-85ee5a357556_PS
VERBOSE: ClientRequestId: ce557cbf-174d-4301-93d4-5ffe082c8413_PS
VERBOSE: ClientRequestId: 31284dad-de2c-4758-a2ef-45962875bfa6_PS
VERBOSE: About to configure the device : win-ff93i74m1e1 ! 
VERBOSE: ClientRequestId: d9c66302-45d8-488a-adda-8ccf957f77d3_PS


TaskId       : 21f530c3-bc47-4591-8c4e-da4d694b751d
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: a94f972c-18ea-40b6-9401-2ad209c0c8b4_PS
AlertNotification              : Microsoft.WindowsAzure.Management.StorSimple.Models.AlertNotificationSettings
Chap                           : Microsoft.WindowsAzure.Management.StorSimple.Models.ChapSettings
DeviceProperties               : Microsoft.WindowsAzure.Management.StorSimple.Models.DeviceInfo
DnsServer                      : Microsoft.WindowsAzure.Management.StorSimple.Models.DnsServerSettings
InstanceId                     : d369ebb4-8b9a-47fc-9a6b-60f371e123ae
Name                           : 
NetInterfaceList               : {}
OperationInProgress            : None
RemoteMgmtSettingsInfo         : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteManagementSettings
RemoteMinishellSecretInfo      : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteMinishellSettings
SecretEncryptionCertThumbprint : 
Snapshot                       : Microsoft.WindowsAzure.Management.StorSimple.Models.SnapshotSettings
TimeServer                     : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeSettings
Type                           : VirtualAppliance
VirtualApplianceProperties     : Microsoft.WindowsAzure.Management.StorSimple.Models.VirtualApplianceInfo
WebProxy                       : Microsoft.WindowsAzure.Management.StorSimple.Models.WebProxySettings

VERBOSE: Successfully updated configuration for device Contoso23 with id d369ebb4-8b9a-47fc-9a6b-60f371e123ae
```

<span data-ttu-id="131b6-109">第一個命令使用 **TimeZoneInfo** .net 類別和標準語法來取得太平洋標準時區，並將該物件儲存在 $TimeZoneInfo 變數中。</span><span class="sxs-lookup"><span data-stu-id="131b6-109">The first command uses the **System.TimeZoneInfo** .NET class and standard syntax to get Pacific Standard Time zone, and stores that object in the $TimeZoneInfo variable.</span></span>

<span data-ttu-id="131b6-110">第二個命令會更新名為 Contoso23 的裝置，以使用 $TimeZoneInfo 中指定的時區。</span><span class="sxs-lookup"><span data-stu-id="131b6-110">The second command updates the device named Contoso23 to use the time zone specified in $TimeZoneInfo.</span></span>
<span data-ttu-id="131b6-111">命令需要機密金鑰才能存取虛擬裝置設定。</span><span class="sxs-lookup"><span data-stu-id="131b6-111">The command requires the secret key to access the virtual device configuration.</span></span>

### <span data-ttu-id="131b6-112">範例2：使用管線運算子更新虛擬裝置</span><span class="sxs-lookup"><span data-stu-id="131b6-112">Example 2: Update a virtual device by using the pipeline operator</span></span>
```
PS C:\> [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" } | Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ=="
```

<span data-ttu-id="131b6-113">這個命令會更新名為 Contoso23 的裝置，以使用該命令所建立的時區。</span><span class="sxs-lookup"><span data-stu-id="131b6-113">This command updates the device named Contoso23 to use the time zone that the command creates.</span></span>
<span data-ttu-id="131b6-114">命令需要機密金鑰才能存取虛擬裝置設定。</span><span class="sxs-lookup"><span data-stu-id="131b6-114">The command requires the secret key to access the virtual device configuration.</span></span>
<span data-ttu-id="131b6-115">這個命令的運作方式與上一個範例相同，只是它會使用管線運算子將時區傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="131b6-115">This command works the same way as the previous example, except that it passes the time zone to the current cmdlet by using the pipeline operator.</span></span>

## <span data-ttu-id="131b6-116">參數</span><span class="sxs-lookup"><span data-stu-id="131b6-116">PARAMETERS</span></span>

### <span data-ttu-id="131b6-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="131b6-117">-AdministratorPassword</span></span>
<span data-ttu-id="131b6-118">指定要設定之虛擬裝置的系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="131b6-118">Specifies the administrator password of the virtual device to configure.</span></span>

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

### <span data-ttu-id="131b6-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="131b6-119">-DeviceName</span></span>
<span data-ttu-id="131b6-120">指定要設定之虛擬裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="131b6-120">Specifies the name of the virtual device to configure.</span></span>

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

### <span data-ttu-id="131b6-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="131b6-121">-Profile</span></span>
<span data-ttu-id="131b6-122">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="131b6-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="131b6-123">-SecretKey</span><span class="sxs-lookup"><span data-stu-id="131b6-123">-SecretKey</span></span>
<span data-ttu-id="131b6-124">指定虛擬裝置的服務加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="131b6-124">Specifies a service encryption key for the virtual device.</span></span>
<span data-ttu-id="131b6-125">當第一個物理裝置註冊至資源時，會產生此金鑰。</span><span class="sxs-lookup"><span data-stu-id="131b6-125">This key is generated when the first physical device is registered with a resource.</span></span>

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

### <span data-ttu-id="131b6-126">-SnapshotManagerPassword</span><span class="sxs-lookup"><span data-stu-id="131b6-126">-SnapshotManagerPassword</span></span>
<span data-ttu-id="131b6-127">指定 snapshot manager 密碼。</span><span class="sxs-lookup"><span data-stu-id="131b6-127">Specifies the snapshot manager password.</span></span>

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

### <span data-ttu-id="131b6-128">-時區</span><span class="sxs-lookup"><span data-stu-id="131b6-128">-TimeZone</span></span>
<span data-ttu-id="131b6-129">指定裝置的時區。</span><span class="sxs-lookup"><span data-stu-id="131b6-129">Specifies a time zone for the device.</span></span>
<span data-ttu-id="131b6-130">您可以使用 **GetSystemTimeZone ( # B1** 方法來建立 **TimeZoneInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="131b6-130">You can create a **TimeZoneInfo** object by using the **GetSystemTimeZone()** method.</span></span>
<span data-ttu-id="131b6-131">例如，這個命令會針對太平洋標準時間建立時區資訊物件： `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span><span class="sxs-lookup"><span data-stu-id="131b6-131">For example, this command creates a time zone information object for Pacific Standard Time: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span></span>

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

### <span data-ttu-id="131b6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="131b6-132">CommonParameters</span></span>
<span data-ttu-id="131b6-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="131b6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="131b6-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="131b6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="131b6-135">輸入</span><span class="sxs-lookup"><span data-stu-id="131b6-135">INPUTS</span></span>

### <span data-ttu-id="131b6-136">TimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="131b6-136">TimeZoneInfo</span></span>
<span data-ttu-id="131b6-137">您可以將 **TimeZoneInfo** 物件輸送到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="131b6-137">You can pipe a **TimeZoneInfo** object to this cmdlet.</span></span>

## <span data-ttu-id="131b6-138">輸出</span><span class="sxs-lookup"><span data-stu-id="131b6-138">OUTPUTS</span></span>

### <span data-ttu-id="131b6-139">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="131b6-139">DeviceJobDetails</span></span>
<span data-ttu-id="131b6-140">這個 Cmdlet 會傳回虛擬裝置的更新裝置詳細資料。</span><span class="sxs-lookup"><span data-stu-id="131b6-140">This cmdlet returns updated device details for the virtual device.</span></span>

## <span data-ttu-id="131b6-141">筆記</span><span class="sxs-lookup"><span data-stu-id="131b6-141">NOTES</span></span>

## <span data-ttu-id="131b6-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="131b6-142">RELATED LINKS</span></span>

[<span data-ttu-id="131b6-143">新-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="131b6-143">New-AzureStorSimpleVirtualDevice</span></span>](./New-AzureStorSimpleVirtualDevice.md)

[<span data-ttu-id="131b6-144">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="131b6-144">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)


