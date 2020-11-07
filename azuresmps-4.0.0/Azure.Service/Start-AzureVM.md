---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C60F78AE-3803-4D9F-A4F3-EAA42052C0E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a0708ca37cdb2b700772da2fe9cb684b8b29a30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967217"
---
# <span data-ttu-id="57c24-101">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="57c24-101">Start-AzureVM</span></span>

## <span data-ttu-id="57c24-102">摘要</span><span class="sxs-lookup"><span data-stu-id="57c24-102">SYNOPSIS</span></span>
<span data-ttu-id="57c24-103">啟動 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="57c24-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="57c24-104">句法</span><span class="sxs-lookup"><span data-stu-id="57c24-104">SYNTAX</span></span>

### <span data-ttu-id="57c24-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="57c24-105">ByName (Default)</span></span>
```
Start-AzureVM [-Name] <String[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="57c24-106">輸出</span><span class="sxs-lookup"><span data-stu-id="57c24-106">Input</span></span>
```
Start-AzureVM -VM <IPersistentVM[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="57c24-107">說明</span><span class="sxs-lookup"><span data-stu-id="57c24-107">DESCRIPTION</span></span>
<span data-ttu-id="57c24-108">**Start-add-azurevm** Cmdlet 會要求 Azure 虛擬機器的開始。</span><span class="sxs-lookup"><span data-stu-id="57c24-108">The **Start-AzureVM** cmdlet requests the start of an Azure virtual machine.</span></span>

## <span data-ttu-id="57c24-109">示例</span><span class="sxs-lookup"><span data-stu-id="57c24-109">EXAMPLES</span></span>

### <span data-ttu-id="57c24-110">範例1：啟動虛擬機器</span><span class="sxs-lookup"><span data-stu-id="57c24-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04"
```

<span data-ttu-id="57c24-111">這個命令會啟動在名為 ContosoService03 的 Azure 服務中執行的名為 VirtualMachine04 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="57c24-111">This command starts the virtual machine named VirtualMachine04 that runs in the Azure service named ContosoService03.</span></span>

### <span data-ttu-id="57c24-112">範例2：使用虛擬電腦物件啟動虛擬機器</span><span class="sxs-lookup"><span data-stu-id="57c24-112">Example 2: Start a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "DatabaseServer" | Start-AzureVM
```

<span data-ttu-id="57c24-113">這個命令會檢索名稱為 DatabaseServer 的虛擬機器的虛擬電腦物件，然後要求啟動該物件。</span><span class="sxs-lookup"><span data-stu-id="57c24-113">This command retrieves the virtual machine object for the virtual machine whose name is DatabaseServer, and then requests to start it.</span></span>

## <span data-ttu-id="57c24-114">參數</span><span class="sxs-lookup"><span data-stu-id="57c24-114">PARAMETERS</span></span>

### <span data-ttu-id="57c24-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="57c24-115">-InformationAction</span></span>
<span data-ttu-id="57c24-116">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="57c24-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="57c24-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="57c24-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="57c24-118">持續</span><span class="sxs-lookup"><span data-stu-id="57c24-118">Continue</span></span>
- <span data-ttu-id="57c24-119">理會</span><span class="sxs-lookup"><span data-stu-id="57c24-119">Ignore</span></span>
- <span data-ttu-id="57c24-120">看</span><span class="sxs-lookup"><span data-stu-id="57c24-120">Inquire</span></span>
- <span data-ttu-id="57c24-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="57c24-121">SilentlyContinue</span></span>
- <span data-ttu-id="57c24-122">停止</span><span class="sxs-lookup"><span data-stu-id="57c24-122">Stop</span></span>
- <span data-ttu-id="57c24-123">封存</span><span class="sxs-lookup"><span data-stu-id="57c24-123">Suspend</span></span>

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

### <span data-ttu-id="57c24-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="57c24-124">-InformationVariable</span></span>
<span data-ttu-id="57c24-125">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="57c24-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="57c24-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="57c24-126">-Name</span></span>
<span data-ttu-id="57c24-127">指定要啟動的虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="57c24-127">Specifies the name of the virtual machine to start.</span></span>

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c24-128">-設定檔</span><span class="sxs-lookup"><span data-stu-id="57c24-128">-Profile</span></span>
<span data-ttu-id="57c24-129">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="57c24-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="57c24-130">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="57c24-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="57c24-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="57c24-131">-ServiceName</span></span>
<span data-ttu-id="57c24-132">指定包含要啟動的虛擬機器之 Azure 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="57c24-132">Specifies the name of the Azure service that contains the virtual machine to start.</span></span>

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

### <span data-ttu-id="57c24-133">-VM</span><span class="sxs-lookup"><span data-stu-id="57c24-133">-VM</span></span>
<span data-ttu-id="57c24-134">指定識別要啟動的虛擬機器的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="57c24-134">Specifies a virtual machine object that identifies the virtual machine to start.</span></span>

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c24-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c24-135">CommonParameters</span></span>
<span data-ttu-id="57c24-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="57c24-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c24-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="57c24-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c24-138">輸入</span><span class="sxs-lookup"><span data-stu-id="57c24-138">INPUTS</span></span>

## <span data-ttu-id="57c24-139">輸出</span><span class="sxs-lookup"><span data-stu-id="57c24-139">OUTPUTS</span></span>

## <span data-ttu-id="57c24-140">筆記</span><span class="sxs-lookup"><span data-stu-id="57c24-140">NOTES</span></span>

## <span data-ttu-id="57c24-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="57c24-141">RELATED LINKS</span></span>

[<span data-ttu-id="57c24-142">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="57c24-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="57c24-143">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="57c24-143">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="57c24-144">Restart-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="57c24-144">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="57c24-145">靜幀</span><span class="sxs-lookup"><span data-stu-id="57c24-145">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="57c24-146">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="57c24-146">Update-AzureVM</span></span>](./Update-AzureVM.md)


