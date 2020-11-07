---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 437889D1-F24F-4BBE-8C56-7C3E48CEA517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86dd38ce7fa55507be3362c1494b88df491a1067
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967237"
---
# <span data-ttu-id="0444d-101">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="0444d-101">Set-AzureVMSize</span></span>

## <span data-ttu-id="0444d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0444d-102">SYNOPSIS</span></span>
<span data-ttu-id="0444d-103">設定 Azure 虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="0444d-103">Sets the size of an Azure virtual machine.</span></span>

## <span data-ttu-id="0444d-104">句法</span><span class="sxs-lookup"><span data-stu-id="0444d-104">SYNTAX</span></span>

```
Set-AzureVMSize [-InstanceSize] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0444d-105">說明</span><span class="sxs-lookup"><span data-stu-id="0444d-105">DESCRIPTION</span></span>
<span data-ttu-id="0444d-106">**AzureVMSize** Cmdlet 會更新虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="0444d-106">The **Set-AzureVMSize** cmdlet updates the size of a virtual machine.</span></span>
<span data-ttu-id="0444d-107">它有兩個參數： *InstanceSize* （這是虛擬電腦的新大小）和 *VM* （即使用 **add-azurevm** Cmdlet 檢索的虛擬機器物件）。</span><span class="sxs-lookup"><span data-stu-id="0444d-107">It has two parameters: *InstanceSize* , which is the new size of the virtual machine, and *VM* , which is a virtual machine object retrieved by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="0444d-108">**AzureVMSize** 的結果可以輸送到 **add-azurevm** Cmdlet，或儲存在變數中供日後使用。</span><span class="sxs-lookup"><span data-stu-id="0444d-108">The result of **Set-AzureVMSize** can be piped to the **Update-AzureVM** cmdlet or stored in a variable for later use.</span></span>
<span data-ttu-id="0444d-109">除非執行 **更新** ，否則不會進行任何實際的變更。</span><span class="sxs-lookup"><span data-stu-id="0444d-109">No actual change is made until **Update-AzureVM** is executed.</span></span>

<span data-ttu-id="0444d-110">注意：此 Cmdlet 會要求重新預配虛擬機器，且可能會取得新的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="0444d-110">Note: This cmdlet will require the virtual machine to be re-provisioned and it might get a new IP address.</span></span>

## <span data-ttu-id="0444d-111">示例</span><span class="sxs-lookup"><span data-stu-id="0444d-111">EXAMPLES</span></span>

### <span data-ttu-id="0444d-112">範例1：設定虛擬機器的大小</span><span class="sxs-lookup"><span data-stu-id="0444d-112">Example 1: Set the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MySvc1" -Name "MyVM3" | Set-AzureVMSize "Small" | Update-AzureVM
```

<span data-ttu-id="0444d-113">這個命令會將虛擬機器更新為「Small」大小。</span><span class="sxs-lookup"><span data-stu-id="0444d-113">This command updates a virtual machine to size "Small".</span></span>

## <span data-ttu-id="0444d-114">參數</span><span class="sxs-lookup"><span data-stu-id="0444d-114">PARAMETERS</span></span>

### <span data-ttu-id="0444d-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0444d-115">-InformationAction</span></span>
<span data-ttu-id="0444d-116">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="0444d-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0444d-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0444d-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0444d-118">持續</span><span class="sxs-lookup"><span data-stu-id="0444d-118">Continue</span></span>
- <span data-ttu-id="0444d-119">理會</span><span class="sxs-lookup"><span data-stu-id="0444d-119">Ignore</span></span>
- <span data-ttu-id="0444d-120">看</span><span class="sxs-lookup"><span data-stu-id="0444d-120">Inquire</span></span>
- <span data-ttu-id="0444d-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0444d-121">SilentlyContinue</span></span>
- <span data-ttu-id="0444d-122">停止</span><span class="sxs-lookup"><span data-stu-id="0444d-122">Stop</span></span>
- <span data-ttu-id="0444d-123">封存</span><span class="sxs-lookup"><span data-stu-id="0444d-123">Suspend</span></span>

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

### <span data-ttu-id="0444d-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0444d-124">-InformationVariable</span></span>
<span data-ttu-id="0444d-125">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="0444d-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0444d-126">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="0444d-126">-InstanceSize</span></span>
<span data-ttu-id="0444d-127">指定虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="0444d-127">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="0444d-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0444d-128">The acceptable values for this parameter are:</span></span>

<span data-ttu-id="0444d-129">--ExtraSmall--中小型--大型--ExtraLarge--A5--A6--A7</span><span class="sxs-lookup"><span data-stu-id="0444d-129">--ExtraSmall --Small --Medium --Large --ExtraLarge --A5 --A6 --A7</span></span>

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

### <span data-ttu-id="0444d-130">-設定檔</span><span class="sxs-lookup"><span data-stu-id="0444d-130">-Profile</span></span>
<span data-ttu-id="0444d-131">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0444d-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0444d-132">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="0444d-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0444d-133">-VM</span><span class="sxs-lookup"><span data-stu-id="0444d-133">-VM</span></span>
<span data-ttu-id="0444d-134">指定這個 Cmdlet 設定大小的永久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="0444d-134">Specifies the persistent virtual machine object that this cmdlet sets the size of.</span></span>

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

### <span data-ttu-id="0444d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0444d-135">CommonParameters</span></span>
<span data-ttu-id="0444d-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0444d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0444d-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0444d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0444d-138">輸入</span><span class="sxs-lookup"><span data-stu-id="0444d-138">INPUTS</span></span>

## <span data-ttu-id="0444d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="0444d-139">OUTPUTS</span></span>

## <span data-ttu-id="0444d-140">筆記</span><span class="sxs-lookup"><span data-stu-id="0444d-140">NOTES</span></span>

## <span data-ttu-id="0444d-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="0444d-141">RELATED LINKS</span></span>

[<span data-ttu-id="0444d-142">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="0444d-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="0444d-143">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="0444d-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


