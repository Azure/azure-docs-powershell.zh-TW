---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8DC10708-09CE-449C-BE20-1E9E49CCE08A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55d9879d6e6768bf3ad409c84a4fc1052d58d8b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967459"
---
# <span data-ttu-id="ddab1-101">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ddab1-101">Update-AzureVM</span></span>

## <span data-ttu-id="ddab1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ddab1-102">SYNOPSIS</span></span>
<span data-ttu-id="ddab1-103">修改 Azure 虛擬機器的設定。</span><span class="sxs-lookup"><span data-stu-id="ddab1-103">Modifies the configuration of an Azure virtual machine.</span></span>

## <span data-ttu-id="ddab1-104">句法</span><span class="sxs-lookup"><span data-stu-id="ddab1-104">SYNTAX</span></span>

```
Update-AzureVM [-Name] <String> -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ddab1-105">說明</span><span class="sxs-lookup"><span data-stu-id="ddab1-105">DESCRIPTION</span></span>
<span data-ttu-id="ddab1-106">**Add-azurevm** Cmdlet 會接受指定虛擬機器的更新資訊，並啟動更新。</span><span class="sxs-lookup"><span data-stu-id="ddab1-106">The **Update-AzureVM** cmdlet accepts update information for the specified virtual machine and initiates the update.</span></span>
<span data-ttu-id="ddab1-107">您可以新增或移除資料磁片、修改資料或作業系統磁片的快取模式、變更網路端點，或變更虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="ddab1-107">You can add or remove data disks, modify the cache mode of data or operating system disks, change the network endpoints, or change the size of the virtual machine.</span></span>

## <span data-ttu-id="ddab1-108">示例</span><span class="sxs-lookup"><span data-stu-id="ddab1-108">EXAMPLES</span></span>

### <span data-ttu-id="ddab1-109">範例1：更新虛擬機器的大小</span><span class="sxs-lookup"><span data-stu-id="ddab1-109">Example 1: Update the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" | Set-AzureVMSize -InstanceSize "Medium" | Update-AzureVM
```

<span data-ttu-id="ddab1-110">這個命令會將名為 VirtualMachine04 的虛擬機器大小（在名為 ContosoService03 的服務中執行）變更為 [中]。</span><span class="sxs-lookup"><span data-stu-id="ddab1-110">This command changes the size of the virtual machine named VirtualMachine04, running in the service named ContosoService03, to Medium.</span></span>

### <span data-ttu-id="ddab1-111">範例2：將資料磁片新增至虛擬機器</span><span class="sxs-lookup"><span data-stu-id="ddab1-111">Example 2: Add a data disk to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine05" | Add-AzureDataDisk -CreateNew -MediaLocation "https://ContosoStore1.blob.core.azure.com/vhds/Disk22.vhd" -DiskSizeInGB 128 -DiskLabel "Data-128" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="ddab1-112">這個命令會將新的資料磁片新增到名為 VirtualMachine05 的虛擬機器，並在名為 ContosoService03 的服務中執行。</span><span class="sxs-lookup"><span data-stu-id="ddab1-112">This command adds a new data disk to the virtual machine named VirtualMachine05, running in the service named ContosoService03.</span></span>

## <span data-ttu-id="ddab1-113">參數</span><span class="sxs-lookup"><span data-stu-id="ddab1-113">PARAMETERS</span></span>

### <span data-ttu-id="ddab1-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ddab1-114">-InformationAction</span></span>
<span data-ttu-id="ddab1-115">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="ddab1-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ddab1-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ddab1-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ddab1-117">持續</span><span class="sxs-lookup"><span data-stu-id="ddab1-117">Continue</span></span>
- <span data-ttu-id="ddab1-118">理會</span><span class="sxs-lookup"><span data-stu-id="ddab1-118">Ignore</span></span>
- <span data-ttu-id="ddab1-119">看</span><span class="sxs-lookup"><span data-stu-id="ddab1-119">Inquire</span></span>
- <span data-ttu-id="ddab1-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ddab1-120">SilentlyContinue</span></span>
- <span data-ttu-id="ddab1-121">停止</span><span class="sxs-lookup"><span data-stu-id="ddab1-121">Stop</span></span>
- <span data-ttu-id="ddab1-122">封存</span><span class="sxs-lookup"><span data-stu-id="ddab1-122">Suspend</span></span>

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

### <span data-ttu-id="ddab1-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ddab1-123">-InformationVariable</span></span>
<span data-ttu-id="ddab1-124">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="ddab1-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ddab1-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ddab1-125">-Name</span></span>
<span data-ttu-id="ddab1-126">指定要更新的虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddab1-126">Specifies the name of the virtual machine to update.</span></span>

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

### <span data-ttu-id="ddab1-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ddab1-127">-Profile</span></span>
<span data-ttu-id="ddab1-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ddab1-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ddab1-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ddab1-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ddab1-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ddab1-130">-ServiceName</span></span>
<span data-ttu-id="ddab1-131">指定 Azure 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddab1-131">Specifies the name of the Azure service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddab1-132">-VM</span><span class="sxs-lookup"><span data-stu-id="ddab1-132">-VM</span></span>
<span data-ttu-id="ddab1-133">指定包含更新設定的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="ddab1-133">Specifies the virtual machine object that includes updated settings.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddab1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddab1-134">CommonParameters</span></span>
<span data-ttu-id="ddab1-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ddab1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddab1-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ddab1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddab1-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ddab1-137">INPUTS</span></span>

## <span data-ttu-id="ddab1-138">輸出</span><span class="sxs-lookup"><span data-stu-id="ddab1-138">OUTPUTS</span></span>

## <span data-ttu-id="ddab1-139">筆記</span><span class="sxs-lookup"><span data-stu-id="ddab1-139">NOTES</span></span>

## <span data-ttu-id="ddab1-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddab1-140">RELATED LINKS</span></span>

[<span data-ttu-id="ddab1-141">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="ddab1-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="ddab1-142">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="ddab1-142">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="ddab1-143">新-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="ddab1-143">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="ddab1-144">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="ddab1-144">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="ddab1-145">Restart-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="ddab1-145">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="ddab1-146">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="ddab1-146">Set-AzureVMSize</span></span>](./Set-AzureVMSize.md)

[<span data-ttu-id="ddab1-147">開始-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="ddab1-147">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="ddab1-148">靜幀</span><span class="sxs-lookup"><span data-stu-id="ddab1-148">Stop-AzureVM</span></span>](./Stop-AzureVM.md)


