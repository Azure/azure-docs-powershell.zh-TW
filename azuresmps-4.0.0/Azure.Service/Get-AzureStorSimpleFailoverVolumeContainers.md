---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BABBA19E-5833-452C-9E36-811EAE7C20F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb326281058f0ff9280c4b87c0530241ece801e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967007"
---
# <span data-ttu-id="bd19c-101">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="bd19c-101">Get-AzureStorSimpleFailoverVolumeContainers</span></span>

## <span data-ttu-id="bd19c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd19c-102">SYNOPSIS</span></span>
<span data-ttu-id="bd19c-103">取得裝置容錯移轉的大量容器群組。</span><span class="sxs-lookup"><span data-stu-id="bd19c-103">Gets the volume container groups for device failover.</span></span>

## <span data-ttu-id="bd19c-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd19c-104">SYNTAX</span></span>

### <span data-ttu-id="bd19c-105">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="bd19c-105">IdentifyById</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bd19c-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="bd19c-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd19c-107">說明</span><span class="sxs-lookup"><span data-stu-id="bd19c-107">DESCRIPTION</span></span>
<span data-ttu-id="bd19c-108">**AzureStorSimpleFailoverVolumeContainers** Cmdlet 會取得裝置容錯移轉的大量容器群組。</span><span class="sxs-lookup"><span data-stu-id="bd19c-108">The **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet gets the volume container groups for device failover.</span></span>
<span data-ttu-id="bd19c-109">將單一 **VolumeContainer** 群組或 **VolumeContainer** 群組陣列傳遞給 **Start AzureStorSimpleDeviceFailover** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bd19c-109">Pass a single **VolumeContainer** group or an array of **VolumeContainer** groups to the **Start-AzureStorSimpleDeviceFailover** cmdlet.</span></span>
<span data-ttu-id="bd19c-110">只有 **IsDCGroupEligibleForDR** 屬性的值為 $True 的群組才能進行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="bd19c-110">Only groups that have a value of $True for the **IsDCGroupEligibleForDR** property are eligible for failover.</span></span>

## <span data-ttu-id="bd19c-111">示例</span><span class="sxs-lookup"><span data-stu-id="bd19c-111">EXAMPLES</span></span>

### <span data-ttu-id="bd19c-112">範例1：取得容錯移轉磁片容器</span><span class="sxs-lookup"><span data-stu-id="bd19c-112">Example 1: Get failover volume containers</span></span>
```
PS C:\>Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7"

DCGroup                    IneligibilityMessage          IsDCGroupEligibleForDR
-------                    --------------------          ----------------------
{VolumeContainer1889078...                                                 True
{VC_01}                    No cloud snapshot found                        False
{VolumeContainer7306959}   No cloud snapshot found                        False
{VolumeContainer407850151} No cloud snapshot found                        False
```

<span data-ttu-id="bd19c-113">這個命令會取得容錯移轉磁片容器。</span><span class="sxs-lookup"><span data-stu-id="bd19c-113">This command gets failover volume containers.</span></span>
<span data-ttu-id="bd19c-114">只有 **IsDCGroupEligibleForDR** 屬性 $True 值的 DCGroups 可用於裝置容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="bd19c-114">Only the DCGroups that have a value of $True for the **IsDCGroupEligibleForDR** property can be used for device failover.</span></span>

## <span data-ttu-id="bd19c-115">參數</span><span class="sxs-lookup"><span data-stu-id="bd19c-115">PARAMETERS</span></span>

### <span data-ttu-id="bd19c-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="bd19c-116">-DeviceId</span></span>
<span data-ttu-id="bd19c-117">指定要在其上執行 Cmdlet 之 StorSimple 裝置的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="bd19c-117">Specifies the instance ID of the StorSimple device on which to run the cmdlet.</span></span>

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

### <span data-ttu-id="bd19c-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="bd19c-118">-DeviceName</span></span>
<span data-ttu-id="bd19c-119">指定要在其上執行 Cmdlet 的 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd19c-119">Specifies the name of the StorSimple device on which to run the cmdlet.</span></span>

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

### <span data-ttu-id="bd19c-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="bd19c-120">-Profile</span></span>
<span data-ttu-id="bd19c-121">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="bd19c-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="bd19c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd19c-122">CommonParameters</span></span>
<span data-ttu-id="bd19c-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd19c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd19c-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bd19c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd19c-125">輸入</span><span class="sxs-lookup"><span data-stu-id="bd19c-125">INPUTS</span></span>

## <span data-ttu-id="bd19c-126">輸出</span><span class="sxs-lookup"><span data-stu-id="bd19c-126">OUTPUTS</span></span>

### <span data-ttu-id="bd19c-127">IList\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="bd19c-127">IList\<DataContainerGroup\></span></span>
<span data-ttu-id="bd19c-128">這個 Cmdlet 會傳回 **VolumeContainer** 群組清單。</span><span class="sxs-lookup"><span data-stu-id="bd19c-128">This cmdlet returns a list of **VolumeContainer** groups.</span></span>

## <span data-ttu-id="bd19c-129">筆記</span><span class="sxs-lookup"><span data-stu-id="bd19c-129">NOTES</span></span>

## <span data-ttu-id="bd19c-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd19c-130">RELATED LINKS</span></span>

[<span data-ttu-id="bd19c-131">開始-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="bd19c-131">Start-AzureStorSimpleDeviceFailoverJob</span></span>](./Start-AzureStorSimpleDeviceFailoverJob.md)

[<span data-ttu-id="bd19c-132">AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="bd19c-132">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)


