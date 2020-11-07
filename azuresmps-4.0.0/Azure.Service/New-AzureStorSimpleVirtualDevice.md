---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F16BCE0C-1F2C-4FB7-972D-28BE3CCD96D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc41efa1901debf2efabf66f8d27f00da7eafe5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966957"
---
# <span data-ttu-id="2e85f-101">New-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="2e85f-101">New-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="2e85f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e85f-102">SYNOPSIS</span></span>
<span data-ttu-id="2e85f-103">建立虛擬 StorSimple 裝置。</span><span class="sxs-lookup"><span data-stu-id="2e85f-103">Creates a virtual StorSimple device.</span></span>

## <span data-ttu-id="2e85f-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e85f-104">SYNTAX</span></span>

### <span data-ttu-id="2e85f-105">CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e85f-105">CreateNewStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 [-StorageAccountName <String>] [-CreateNewStorageAccount] [-PersistAzureVMOnFailrue]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2e85f-106">UseExistingStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e85f-106">UseExistingStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 -StorageAccountName <String> [-PersistAzureVMOnFailrue] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2e85f-107">說明</span><span class="sxs-lookup"><span data-stu-id="2e85f-107">DESCRIPTION</span></span>
<span data-ttu-id="2e85f-108">**新的-AzureStorSimpleVirtualDevice** Cmdlet 會建立虛擬 StorSimple 裝置。</span><span class="sxs-lookup"><span data-stu-id="2e85f-108">The **New-AzureStorSimpleVirtualDevice** cmdlet creates a virtual StorSimple device.</span></span>
<span data-ttu-id="2e85f-109">指定裝置的裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="2e85f-109">Specify a device name for the device.</span></span>
<span data-ttu-id="2e85f-110">針對相同訂閱中的虛擬網路指定虛擬網路和子網詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2e85f-110">Specify virtual network and subnet details for the virtual network in the same subscription.</span></span>
<span data-ttu-id="2e85f-111">Geo 應該與建立 StorSimple 資源的地理位置相符。</span><span class="sxs-lookup"><span data-stu-id="2e85f-111">The geo should match the geo in which the StorSimple resource is created.</span></span>
<span data-ttu-id="2e85f-112">若要使用此虛擬裝置的現有儲存空間帳戶，請指定名稱。</span><span class="sxs-lookup"><span data-stu-id="2e85f-112">To use an existing storage account for this virtual device, specify the name.</span></span>
<span data-ttu-id="2e85f-113">若要為此虛擬裝置建立新的儲存空間帳戶，請指定 *StorageAccountName* 和 *CreateNewStorageAccount* 參數。</span><span class="sxs-lookup"><span data-stu-id="2e85f-113">To create a new storage account for this virtual device, specify both the *StorageAccountName* and the *CreateNewStorageAccount* parameters.</span></span>

## <span data-ttu-id="2e85f-114">示例</span><span class="sxs-lookup"><span data-stu-id="2e85f-114">EXAMPLES</span></span>

### <span data-ttu-id="2e85f-115">範例1：使用新帳戶和現有的網路建立虛擬裝置</span><span class="sxs-lookup"><span data-stu-id="2e85f-115">Example 1: Create a virtual device with a new account and an existing network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "Contosodevice02" -VirtualNetworkName "Saas2vpn" -SubNetName "TenantSubnet" -StorageAccountName "AzureTenant04" -CreateNewStorageAccount
64e4c564-b0ac-44b0-afb4-adf28ac24ad0
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 64e4c564-b0ac-44b0-afb4-adf28ac24ad0 for tracking the job's status
```

<span data-ttu-id="2e85f-116">這個命令會建立使用新儲存空間帳戶和現有虛擬網路的虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="2e85f-116">This command creates a virtual device that uses a new storage account and an existing virtual network.</span></span>

### <span data-ttu-id="2e85f-117">範例2：使用現有的帳戶和虛擬網路建立虛擬裝置</span><span class="sxs-lookup"><span data-stu-id="2e85f-117">Example 2: Create a virtual device with an existing account and virtual network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "ContosoDevice07" -VirtualNetworkName "Saas2vpn" -SubNetName TenantSubnet -StorageAccountName azurecisbvtdnd
2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf for tracking the job's status
```

<span data-ttu-id="2e85f-118">這個命令會建立使用現有儲存空間帳戶和現有虛擬網路的虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="2e85f-118">This command creates a virtual device that uses an existing storage account and an existing virtual network.</span></span>

## <span data-ttu-id="2e85f-119">參數</span><span class="sxs-lookup"><span data-stu-id="2e85f-119">PARAMETERS</span></span>

### <span data-ttu-id="2e85f-120">-CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e85f-120">-CreateNewStorageAccount</span></span>
<span data-ttu-id="2e85f-121">表示此 Cmdlet 會建立新的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="2e85f-121">Indicates that this cmdlet creates a new storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e85f-122">-PersistAzureVMOnFailrue</span><span class="sxs-lookup"><span data-stu-id="2e85f-122">-PersistAzureVMOnFailrue</span></span>
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

### <span data-ttu-id="2e85f-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="2e85f-123">-Profile</span></span>
<span data-ttu-id="2e85f-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="2e85f-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2e85f-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="2e85f-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2e85f-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2e85f-126">-StorageAccountName</span></span>
<span data-ttu-id="2e85f-127">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e85f-127">Specifies the name of a storage account.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UseExistingStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e85f-128">-SubNetName</span><span class="sxs-lookup"><span data-stu-id="2e85f-128">-SubNetName</span></span>
<span data-ttu-id="2e85f-129">指定虛擬子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e85f-129">Specifies the name of a virtual subnet.</span></span>

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

### <span data-ttu-id="2e85f-130">-VirtualDeviceName</span><span class="sxs-lookup"><span data-stu-id="2e85f-130">-VirtualDeviceName</span></span>
<span data-ttu-id="2e85f-131">指定虛擬裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e85f-131">Specifies a name for the virtual device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e85f-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="2e85f-132">-VirtualNetworkName</span></span>
<span data-ttu-id="2e85f-133">指定虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e85f-133">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VNetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e85f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e85f-134">CommonParameters</span></span>
<span data-ttu-id="2e85f-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e85f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e85f-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2e85f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e85f-137">輸入</span><span class="sxs-lookup"><span data-stu-id="2e85f-137">INPUTS</span></span>

## <span data-ttu-id="2e85f-138">輸出</span><span class="sxs-lookup"><span data-stu-id="2e85f-138">OUTPUTS</span></span>

### <span data-ttu-id="2e85f-139">字串</span><span class="sxs-lookup"><span data-stu-id="2e85f-139">String</span></span>
<span data-ttu-id="2e85f-140">這個 Cmdlet 會傳回建立虛擬裝置作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2e85f-140">This cmdlet returns the ID of the job that creates the virtual device.</span></span>
<span data-ttu-id="2e85f-141">您可以使用此識別碼來追蹤使用 Get-AzureStorSimpleJob Cmdlet 的進度。</span><span class="sxs-lookup"><span data-stu-id="2e85f-141">You can use this ID to track the progress using the Get-AzureStorSimpleJob cmdlet.</span></span>

## <span data-ttu-id="2e85f-142">筆記</span><span class="sxs-lookup"><span data-stu-id="2e85f-142">NOTES</span></span>

## <span data-ttu-id="2e85f-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e85f-143">RELATED LINKS</span></span>

[<span data-ttu-id="2e85f-144">AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="2e85f-144">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="2e85f-145">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="2e85f-145">Set-AzureStorSimpleVirtualDevice</span></span>](./Set-AzureStorSimpleVirtualDevice.md)


