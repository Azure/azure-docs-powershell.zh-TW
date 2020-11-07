---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 455DB2C0-08A0-4D62-B8EE-7C3DB9AD8A8C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85040f07914aef02355f69baab093c75ce7e4afd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966962"
---
# <span data-ttu-id="a10bc-101">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a10bc-101">Remove-AzureVM</span></span>

## <span data-ttu-id="a10bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a10bc-102">SYNOPSIS</span></span>
<span data-ttu-id="a10bc-103">移除 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a10bc-103">Removes an Azure virtual machine.</span></span>

## <span data-ttu-id="a10bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="a10bc-104">SYNTAX</span></span>

```
Remove-AzureVM [-Name] <String> [-DeleteVHD] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a10bc-105">說明</span><span class="sxs-lookup"><span data-stu-id="a10bc-105">DESCRIPTION</span></span>
<span data-ttu-id="a10bc-106">**Add-azurevm** Cmdlet 會刪除 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a10bc-106">The **Remove-AzureVM** cmdlet deletes an Azure virtual machine.</span></span>
<span data-ttu-id="a10bc-107">此程式不會刪除在該虛擬機器上裝載之磁片的基礎 .vhd 檔案。</span><span class="sxs-lookup"><span data-stu-id="a10bc-107">This process does not delete the underlying .vhd files of the disks mounted on that virtual machine.</span></span>

## <span data-ttu-id="a10bc-108">示例</span><span class="sxs-lookup"><span data-stu-id="a10bc-108">EXAMPLES</span></span>

### <span data-ttu-id="a10bc-109">範例1：從服務移除虛擬機器</span><span class="sxs-lookup"><span data-stu-id="a10bc-109">Example 1: Remove a virtual machine from a service</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine03"
```

<span data-ttu-id="a10bc-110">這個命令會移除名為 VirtualMachine03 的虛擬機器，在 ContosoService03 服務中執行。</span><span class="sxs-lookup"><span data-stu-id="a10bc-110">This command removes the virtual machine named VirtualMachine03 that runs in the ContosoService03 service.</span></span>

### <span data-ttu-id="a10bc-111">範例2：移除虛擬機器並刪除 .vhd 檔案</span><span class="sxs-lookup"><span data-stu-id="a10bc-111">Example 2: Remove a virtual machine and delete the .vhd files</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" -DeleteVHD
```

<span data-ttu-id="a10bc-112">這個命令會移除在 ContosoService03 服務中執行的 VirtualMachine04 虛擬機器，並指定使用 *DeleteVHD* 參數來移除 .vhd 檔案。</span><span class="sxs-lookup"><span data-stu-id="a10bc-112">This command removes the VirtualMachine04 virtual machine that runs in the ContosoService03 service, and specifies to remove the .vhd files using the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="a10bc-113">參數</span><span class="sxs-lookup"><span data-stu-id="a10bc-113">PARAMETERS</span></span>

### <span data-ttu-id="a10bc-114">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="a10bc-114">-DeleteVHD</span></span>
<span data-ttu-id="a10bc-115">指定此 Cmdlet 是否移除虛擬機器和基礎磁片 blob。</span><span class="sxs-lookup"><span data-stu-id="a10bc-115">Specifies whether this cmdlet removes the virtual machine and the underlying disk blobs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a10bc-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a10bc-116">-InformationAction</span></span>
<span data-ttu-id="a10bc-117">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="a10bc-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a10bc-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a10bc-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a10bc-119">持續</span><span class="sxs-lookup"><span data-stu-id="a10bc-119">Continue</span></span>
- <span data-ttu-id="a10bc-120">理會</span><span class="sxs-lookup"><span data-stu-id="a10bc-120">Ignore</span></span>
- <span data-ttu-id="a10bc-121">看</span><span class="sxs-lookup"><span data-stu-id="a10bc-121">Inquire</span></span>
- <span data-ttu-id="a10bc-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a10bc-122">SilentlyContinue</span></span>
- <span data-ttu-id="a10bc-123">停止</span><span class="sxs-lookup"><span data-stu-id="a10bc-123">Stop</span></span>
- <span data-ttu-id="a10bc-124">封存</span><span class="sxs-lookup"><span data-stu-id="a10bc-124">Suspend</span></span>

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

### <span data-ttu-id="a10bc-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a10bc-125">-InformationVariable</span></span>
<span data-ttu-id="a10bc-126">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="a10bc-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a10bc-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="a10bc-127">-Name</span></span>
<span data-ttu-id="a10bc-128">指定要移除的虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a10bc-128">Specifies the name of the virtual machine being removed.</span></span>

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

### <span data-ttu-id="a10bc-129">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a10bc-129">-Profile</span></span>
<span data-ttu-id="a10bc-130">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a10bc-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a10bc-131">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a10bc-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a10bc-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a10bc-132">-ServiceName</span></span>
<span data-ttu-id="a10bc-133">指定要從中移除虛擬機器之 Azure 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="a10bc-133">Specifies the name of the Azure service from which the virtual machine is being removed.</span></span>

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

### <span data-ttu-id="a10bc-134">-確認</span><span class="sxs-lookup"><span data-stu-id="a10bc-134">-Confirm</span></span>
<span data-ttu-id="a10bc-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a10bc-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a10bc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a10bc-136">-WhatIf</span></span>
<span data-ttu-id="a10bc-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a10bc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a10bc-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a10bc-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a10bc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a10bc-139">CommonParameters</span></span>
<span data-ttu-id="a10bc-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a10bc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a10bc-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a10bc-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a10bc-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a10bc-142">INPUTS</span></span>

## <span data-ttu-id="a10bc-143">輸出</span><span class="sxs-lookup"><span data-stu-id="a10bc-143">OUTPUTS</span></span>

## <span data-ttu-id="a10bc-144">筆記</span><span class="sxs-lookup"><span data-stu-id="a10bc-144">NOTES</span></span>

## <span data-ttu-id="a10bc-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="a10bc-145">RELATED LINKS</span></span>

[<span data-ttu-id="a10bc-146">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="a10bc-146">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="a10bc-147">新-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="a10bc-147">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="a10bc-148">Restart-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="a10bc-148">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="a10bc-149">開始-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="a10bc-149">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="a10bc-150">靜幀</span><span class="sxs-lookup"><span data-stu-id="a10bc-150">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="a10bc-151">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="a10bc-151">Update-AzureVM</span></span>](./Update-AzureVM.md)


