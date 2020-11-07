---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6AFD3971-460D-4F6A-B266-6ED98DC81CD4
online version: ''
schema: 2.0.0
ms.openlocfilehash: c007e3a318067f29da6ea710c25cf2c52d5df2b4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967685"
---
# <span data-ttu-id="9f257-101">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9f257-101">Move-AzureStorageAccount</span></span>

## <span data-ttu-id="9f257-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9f257-102">SYNOPSIS</span></span>
<span data-ttu-id="9f257-103">將儲存空間帳戶遷移至 Azure 資源管理器堆疊。</span><span class="sxs-lookup"><span data-stu-id="9f257-103">Migrates a storage account to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="9f257-104">句法</span><span class="sxs-lookup"><span data-stu-id="9f257-104">SYNTAX</span></span>

### <span data-ttu-id="9f257-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f257-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Validate] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9f257-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f257-106">AbortMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Abort] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9f257-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f257-107">CommitMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Commit] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9f257-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f257-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Prepare] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9f257-109">說明</span><span class="sxs-lookup"><span data-stu-id="9f257-109">DESCRIPTION</span></span>
<span data-ttu-id="9f257-110">**AzureStorageAccount** Cmdlet 會將儲存空間帳戶遷移至 Azure 資源管理器堆疊中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="9f257-110">The **Move-AzureStorageAccount** cmdlet migrates a storage account to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="9f257-111">示例</span><span class="sxs-lookup"><span data-stu-id="9f257-111">EXAMPLES</span></span>

### <span data-ttu-id="9f257-112">範例1：準備儲存帳戶遷移</span><span class="sxs-lookup"><span data-stu-id="9f257-112">Example 1: Prepare storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Prepare -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="9f257-113">這個命令準備將名為 ContosoStorageName 的儲存空間帳戶遷移至 Azure 資源管理器堆疊。</span><span class="sxs-lookup"><span data-stu-id="9f257-113">This command prepares the storage account named ContosoStorageName for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="9f257-114">範例2：啟動儲存帳戶遷移</span><span class="sxs-lookup"><span data-stu-id="9f257-114">Example 2: Start storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Commit -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="9f257-115">這個命令會開始將名為 ContosoStorageName 的儲存空間帳戶遷移至 Azure 資源管理器堆疊。</span><span class="sxs-lookup"><span data-stu-id="9f257-115">This command starts migration of the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="9f257-116">範例3：驗證儲存帳戶遷移</span><span class="sxs-lookup"><span data-stu-id="9f257-116">Example 3: Validate storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Validate -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="9f257-117">這個命令會將名為 ContosoStorageName 的儲存空間帳戶的遷移驗證到 Azure 資源管理器堆疊。</span><span class="sxs-lookup"><span data-stu-id="9f257-117">This command validates migration for the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="9f257-118">參數</span><span class="sxs-lookup"><span data-stu-id="9f257-118">PARAMETERS</span></span>

### <span data-ttu-id="9f257-119">-中止</span><span class="sxs-lookup"><span data-stu-id="9f257-119">-Abort</span></span>
<span data-ttu-id="9f257-120">表示此 Cmdlet 會取消儲存空間帳戶遷移。</span><span class="sxs-lookup"><span data-stu-id="9f257-120">Indicates that this cmdlet cancels the storage account migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f257-121">-認可</span><span class="sxs-lookup"><span data-stu-id="9f257-121">-Commit</span></span>
<span data-ttu-id="9f257-122">表示此 Cmdlet 會啟動儲存空間帳戶遷移。</span><span class="sxs-lookup"><span data-stu-id="9f257-122">Indicates that this cmdlet starts the storage account migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f257-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9f257-123">-InformationAction</span></span>
<span data-ttu-id="9f257-124">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="9f257-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9f257-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9f257-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9f257-126">持續</span><span class="sxs-lookup"><span data-stu-id="9f257-126">Continue</span></span>
- <span data-ttu-id="9f257-127">理會</span><span class="sxs-lookup"><span data-stu-id="9f257-127">Ignore</span></span>
- <span data-ttu-id="9f257-128">看</span><span class="sxs-lookup"><span data-stu-id="9f257-128">Inquire</span></span>
- <span data-ttu-id="9f257-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9f257-129">SilentlyContinue</span></span>
- <span data-ttu-id="9f257-130">停止</span><span class="sxs-lookup"><span data-stu-id="9f257-130">Stop</span></span>
- <span data-ttu-id="9f257-131">封存</span><span class="sxs-lookup"><span data-stu-id="9f257-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f257-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9f257-132">-InformationVariable</span></span>
<span data-ttu-id="9f257-133">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="9f257-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f257-134">-準備</span><span class="sxs-lookup"><span data-stu-id="9f257-134">-Prepare</span></span>
<span data-ttu-id="9f257-135">表示此 Cmdlet 會為遷移準備儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="9f257-135">Indicates that this cmdlet prepares the storage account for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f257-136">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9f257-136">-Profile</span></span>
<span data-ttu-id="9f257-137">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9f257-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9f257-138">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="9f257-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9f257-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9f257-139">-StorageAccountName</span></span>
<span data-ttu-id="9f257-140">指定此 Cmdlet 遷移的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9f257-140">Specifies the name of the storage account that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f257-141">-驗證</span><span class="sxs-lookup"><span data-stu-id="9f257-141">-Validate</span></span>
<span data-ttu-id="9f257-142">指定此 Cmdlet 會驗證要遷移的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="9f257-142">Specifies that this cmdlet validates the storage account for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f257-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f257-143">CommonParameters</span></span>
<span data-ttu-id="9f257-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9f257-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f257-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9f257-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f257-146">輸入</span><span class="sxs-lookup"><span data-stu-id="9f257-146">INPUTS</span></span>

## <span data-ttu-id="9f257-147">輸出</span><span class="sxs-lookup"><span data-stu-id="9f257-147">OUTPUTS</span></span>

## <span data-ttu-id="9f257-148">筆記</span><span class="sxs-lookup"><span data-stu-id="9f257-148">NOTES</span></span>

## <span data-ttu-id="9f257-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f257-149">RELATED LINKS</span></span>

[<span data-ttu-id="9f257-150">移動流覽 AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9f257-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="9f257-151">移動流覽 AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="9f257-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="9f257-152">移動流覽 AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="9f257-152">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="9f257-153">移動流覽 AzureService</span><span class="sxs-lookup"><span data-stu-id="9f257-153">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="9f257-154">移動流覽 AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9f257-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


