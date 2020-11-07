---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 9436E1AB-870F-4717-ABE0-55A90C07F7E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 555ce014bbbf7174b3f7142cf7e2f217317eadc6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967737"
---
# <span data-ttu-id="4ad5d-101">Get-AzureStorSimpleDeviceConnectedInitiator</span><span class="sxs-lookup"><span data-stu-id="4ad5d-101">Get-AzureStorSimpleDeviceConnectedInitiator</span></span>

## <span data-ttu-id="4ad5d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ad5d-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad5d-103">取得 StorSimple 裝置可用的 iSCSI 連線。</span><span class="sxs-lookup"><span data-stu-id="4ad5d-103">Gets the iSCSI connections available for a StorSimple device.</span></span>

## <span data-ttu-id="4ad5d-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ad5d-104">SYNTAX</span></span>

### <span data-ttu-id="4ad5d-105">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="4ad5d-105">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4ad5d-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="4ad5d-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ad5d-107">說明</span><span class="sxs-lookup"><span data-stu-id="4ad5d-107">DESCRIPTION</span></span>
<span data-ttu-id="4ad5d-108">**AzureStorSimpleDeviceConnectedInitiator** Cmdlet 會取得適用于 StorSimple 裝置的 iSCSI 連線清單。</span><span class="sxs-lookup"><span data-stu-id="4ad5d-108">The **Get-AzureStorSimpleDeviceConnectedInitiator** cmdlet gets a list of the iSCSI connections available for a StorSimple device.</span></span>
<span data-ttu-id="4ad5d-109">這個 Cmdlet 傳回的 iSCSI 連線物件包含下列屬性：</span><span class="sxs-lookup"><span data-stu-id="4ad5d-109">The iSCSI connection objects that this cmdlet returns contain the following properties:</span></span>

- <span data-ttu-id="4ad5d-110">**AcrInstanceId**</span><span class="sxs-lookup"><span data-stu-id="4ad5d-110">**AcrInstanceId**</span></span>
- <span data-ttu-id="4ad5d-111">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="4ad5d-111">**AcrName**</span></span>
- <span data-ttu-id="4ad5d-112">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="4ad5d-112">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="4ad5d-113">**InitiatorAddress**</span><span class="sxs-lookup"><span data-stu-id="4ad5d-113">**InitiatorAddress**</span></span>
- <span data-ttu-id="4ad5d-114">**交互**</span><span class="sxs-lookup"><span data-stu-id="4ad5d-114">**Interfaces**</span></span>
- <span data-ttu-id="4ad5d-115">**Iqn**</span><span class="sxs-lookup"><span data-stu-id="4ad5d-115">**Iqn**</span></span>
- <span data-ttu-id="4ad5d-116">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="4ad5d-116">**IscsiConnectionId**</span></span>

<span data-ttu-id="4ad5d-117">這個 Cmdlet 只會在為裝置開啟 iSCSI 連線時取得連線物件。</span><span class="sxs-lookup"><span data-stu-id="4ad5d-117">This cmdlet gets connection object only if iSCSI connections are turned on for the device.</span></span>
<span data-ttu-id="4ad5d-118">根據預設，會關閉連線。</span><span class="sxs-lookup"><span data-stu-id="4ad5d-118">By default, connections are turned off.</span></span>

## <span data-ttu-id="4ad5d-119">示例</span><span class="sxs-lookup"><span data-stu-id="4ad5d-119">EXAMPLES</span></span>

### <span data-ttu-id="4ad5d-120">範例1：取得裝置的所有連線</span><span class="sxs-lookup"><span data-stu-id="4ad5d-120">Example 1: Get all connections for a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: bec615b9-79ab-4671-88b0-287adeb6bf68_PS
VERBOSE: ClientRequestId: ef976c58-2660-41c8-aa15-c84e70c9d01c_PS
VERBOSE: ClientRequestId: 9b306b96-8e76-47ed-beda-d3bd2fb2bb82_PS
VERBOSE: ClientRequestId: 0f4fc743-0b60-45da-a45a-27f4b0f32bd2_PS

AcrInstanceId      : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
AcrName            : Contoso63-AppVm
AllowedVolumeNames : {Policyvolume1_Default}
InitiatorAddress   : 
Interfaces         : {Data0}
Iqn                : iqn10
IscsiConnectionId  : cfc144cb-00f1-44b1-9655-80b431f2161b

VERBOSE: 1 Iscsi Connection found!
```

<span data-ttu-id="4ad5d-121">這個命令會取得名為 Contoso63-AppVm 的裝置的所有 iSCSI 連線。</span><span class="sxs-lookup"><span data-stu-id="4ad5d-121">This command gets all iSCSI connections for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="4ad5d-122">這個命令只會在為裝置開啟連線時，才會傳回連線。</span><span class="sxs-lookup"><span data-stu-id="4ad5d-122">This command returns connections only if connections are turned on for the device.</span></span>

## <span data-ttu-id="4ad5d-123">參數</span><span class="sxs-lookup"><span data-stu-id="4ad5d-123">PARAMETERS</span></span>

### <span data-ttu-id="4ad5d-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="4ad5d-124">-DeviceId</span></span>
<span data-ttu-id="4ad5d-125">指定要取得 iSCSI 啟動器的 StorSimple 裝置實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ad5d-125">Specifies the instance ID of the StorSimple device from which to get iSCSI initiators.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad5d-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4ad5d-126">-DeviceName</span></span>
<span data-ttu-id="4ad5d-127">指定要取得 iSCSI 啟動器之 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ad5d-127">Specifies the name of the StorSimple device from which to get iSCSI initiators.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad5d-128">-設定檔</span><span class="sxs-lookup"><span data-stu-id="4ad5d-128">-Profile</span></span>
<span data-ttu-id="4ad5d-129">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4ad5d-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="4ad5d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad5d-130">CommonParameters</span></span>
<span data-ttu-id="4ad5d-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ad5d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad5d-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4ad5d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad5d-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4ad5d-133">INPUTS</span></span>

### <span data-ttu-id="4ad5d-134">所有</span><span class="sxs-lookup"><span data-stu-id="4ad5d-134">None</span></span>

## <span data-ttu-id="4ad5d-135">輸出</span><span class="sxs-lookup"><span data-stu-id="4ad5d-135">OUTPUTS</span></span>

### <span data-ttu-id="4ad5d-136">清單\<IscsiConnection\></span><span class="sxs-lookup"><span data-stu-id="4ad5d-136">List\<IscsiConnection\></span></span>
<span data-ttu-id="4ad5d-137">這個 Cmdlet 會傳回包含下列屬性的 iSCSI 連線物件：</span><span class="sxs-lookup"><span data-stu-id="4ad5d-137">This cmdlet returns an iSCSI connection object that contains the following properties:</span></span> 

- <span data-ttu-id="4ad5d-138">**AcrInstanceId**</span><span class="sxs-lookup"><span data-stu-id="4ad5d-138">**AcrInstanceId**</span></span>
- <span data-ttu-id="4ad5d-139">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="4ad5d-139">**AcrName**</span></span>
- <span data-ttu-id="4ad5d-140">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="4ad5d-140">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="4ad5d-141">**InitiatorAddress**</span><span class="sxs-lookup"><span data-stu-id="4ad5d-141">**InitiatorAddress**</span></span>
- <span data-ttu-id="4ad5d-142">**交互**</span><span class="sxs-lookup"><span data-stu-id="4ad5d-142">**Interfaces**</span></span>
- <span data-ttu-id="4ad5d-143">**Iqn**</span><span class="sxs-lookup"><span data-stu-id="4ad5d-143">**Iqn**</span></span>
- <span data-ttu-id="4ad5d-144">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="4ad5d-144">**IscsiConnectionId**</span></span>

## <span data-ttu-id="4ad5d-145">筆記</span><span class="sxs-lookup"><span data-stu-id="4ad5d-145">NOTES</span></span>

## <span data-ttu-id="4ad5d-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ad5d-146">RELATED LINKS</span></span>

[<span data-ttu-id="4ad5d-147">AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="4ad5d-147">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)


