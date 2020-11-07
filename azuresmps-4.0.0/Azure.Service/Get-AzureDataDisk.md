---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2A8BE3EB-4929-4B40-82EA-5434C09A5251
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1974de3f5c4bf39aa32100e67bb04642ebcfe3da
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967097"
---
# <span data-ttu-id="cef11-101">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="cef11-101">Get-AzureDataDisk</span></span>

## <span data-ttu-id="cef11-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cef11-102">SYNOPSIS</span></span>
<span data-ttu-id="cef11-103">取得 Azure 資料磁片。</span><span class="sxs-lookup"><span data-stu-id="cef11-103">Gets Azure data disks.</span></span>

## <span data-ttu-id="cef11-104">句法</span><span class="sxs-lookup"><span data-stu-id="cef11-104">SYNTAX</span></span>

```
Get-AzureDataDisk [[-Lun] <Int32>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cef11-105">說明</span><span class="sxs-lookup"><span data-stu-id="cef11-105">DESCRIPTION</span></span>
<span data-ttu-id="cef11-106">**AzureDataDisk** Cmdlet 會取得代表 Azure 虛擬機器上的資料磁片的物件。</span><span class="sxs-lookup"><span data-stu-id="cef11-106">The **Get-AzureDataDisk** cmdlet gets an object that represents the data disks on an Azure virtual machine.</span></span>
<span data-ttu-id="cef11-107">若要取得特定資料磁片物件，請指定磁片的邏輯單元號碼 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="cef11-107">To get a specific data disk object, specify the logical unit number (LUN) of the disk.</span></span>

## <span data-ttu-id="cef11-108">示例</span><span class="sxs-lookup"><span data-stu-id="cef11-108">EXAMPLES</span></span>

### <span data-ttu-id="cef11-109">範例1：取得虛擬機器的所有資料磁片</span><span class="sxs-lookup"><span data-stu-id="cef11-109">Example 1: Get all data disks for a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk
```

<span data-ttu-id="cef11-110">這個命令會透過使用 **VirtualMachine07 Cmdlet，** 在名為 ContosoService 的服務中，取得名為的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="cef11-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="cef11-111">命令會使用管線運算子，將虛擬機器傳至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cef11-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cef11-112">目前的 Cmdlet 會取得此虛擬機器的所有資料磁片。</span><span class="sxs-lookup"><span data-stu-id="cef11-112">The current cmdlet gets all the data disks for this virtual machine.</span></span>

### <span data-ttu-id="cef11-113">範例2：取得 vituralvirtual machinevirtual 的特定資料磁片</span><span class="sxs-lookup"><span data-stu-id="cef11-113">Example 2: Get a specific data disk for a vituralvirtual machinevirtual</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk -LUN 2
```

<span data-ttu-id="cef11-114">這個命令會在名為 ContosoService 的服務中取得名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="cef11-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="cef11-115">該命令會將虛擬機器傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cef11-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="cef11-116">目前的 Cmdlet 會取得擁有 LUN 2 的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="cef11-116">The current cmdlet gets the data disk that has the LUN 2.</span></span>

## <span data-ttu-id="cef11-117">參數</span><span class="sxs-lookup"><span data-stu-id="cef11-117">PARAMETERS</span></span>

### <span data-ttu-id="cef11-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="cef11-118">-InformationAction</span></span>
<span data-ttu-id="cef11-119">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="cef11-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cef11-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="cef11-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cef11-121">持續</span><span class="sxs-lookup"><span data-stu-id="cef11-121">Continue</span></span>
- <span data-ttu-id="cef11-122">理會</span><span class="sxs-lookup"><span data-stu-id="cef11-122">Ignore</span></span>
- <span data-ttu-id="cef11-123">看</span><span class="sxs-lookup"><span data-stu-id="cef11-123">Inquire</span></span>
- <span data-ttu-id="cef11-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cef11-124">SilentlyContinue</span></span>
- <span data-ttu-id="cef11-125">停止</span><span class="sxs-lookup"><span data-stu-id="cef11-125">Stop</span></span>
- <span data-ttu-id="cef11-126">封存</span><span class="sxs-lookup"><span data-stu-id="cef11-126">Suspend</span></span>

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

### <span data-ttu-id="cef11-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cef11-127">-InformationVariable</span></span>
<span data-ttu-id="cef11-128">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="cef11-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cef11-129">-Lun</span><span class="sxs-lookup"><span data-stu-id="cef11-129">-Lun</span></span>
<span data-ttu-id="cef11-130">指定虛擬機器中資料磁碟機的 LUN。</span><span class="sxs-lookup"><span data-stu-id="cef11-130">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="cef11-131">有效值為：0到15。</span><span class="sxs-lookup"><span data-stu-id="cef11-131">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef11-132">-設定檔</span><span class="sxs-lookup"><span data-stu-id="cef11-132">-Profile</span></span>
<span data-ttu-id="cef11-133">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="cef11-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cef11-134">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="cef11-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cef11-135">-VM</span><span class="sxs-lookup"><span data-stu-id="cef11-135">-VM</span></span>
<span data-ttu-id="cef11-136">指定此 Cmdlet 取得資料磁片的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="cef11-136">Specifies the virtual machine object for which this cmdlet gets data disks.</span></span>
<span data-ttu-id="cef11-137">若要取得虛擬機器物件，請使用 **add-azurevm** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cef11-137">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cef11-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef11-138">CommonParameters</span></span>
<span data-ttu-id="cef11-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cef11-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef11-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cef11-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef11-141">輸入</span><span class="sxs-lookup"><span data-stu-id="cef11-141">INPUTS</span></span>

## <span data-ttu-id="cef11-142">輸出</span><span class="sxs-lookup"><span data-stu-id="cef11-142">OUTPUTS</span></span>

## <span data-ttu-id="cef11-143">筆記</span><span class="sxs-lookup"><span data-stu-id="cef11-143">NOTES</span></span>

## <span data-ttu-id="cef11-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="cef11-144">RELATED LINKS</span></span>

[<span data-ttu-id="cef11-145">附加 AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="cef11-145">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="cef11-146">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="cef11-146">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="cef11-147">移除-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="cef11-147">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="cef11-148">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="cef11-148">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)


