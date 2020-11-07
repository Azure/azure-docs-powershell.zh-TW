---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C9470E5-21D2-4AF5-9F11-F66F94B133C0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23f4511f8e0439c1581cc388843a37266092f4d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967900"
---
# <span data-ttu-id="418d1-101">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="418d1-101">Remove-AzureVMImage</span></span>

## <span data-ttu-id="418d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="418d1-102">SYNOPSIS</span></span>
<span data-ttu-id="418d1-103">從影像存放庫移除作業系統影像。</span><span class="sxs-lookup"><span data-stu-id="418d1-103">Removes an operating system image from the image repository.</span></span>

## <span data-ttu-id="418d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="418d1-104">SYNTAX</span></span>

```
Remove-AzureVMImage [-ImageName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="418d1-105">說明</span><span class="sxs-lookup"><span data-stu-id="418d1-105">DESCRIPTION</span></span>
<span data-ttu-id="418d1-106">**AzureVMImage** Cmdlet 會從影像存放庫中移除作業系統影像。</span><span class="sxs-lookup"><span data-stu-id="418d1-106">The **Remove-AzureVMImage** cmdlet removes an operating system image from the image repository.</span></span>
<span data-ttu-id="418d1-107">根據預設，這個 Cmdlet 不會從儲存空間帳戶中刪除關聯的物理影像 blob。</span><span class="sxs-lookup"><span data-stu-id="418d1-107">By default, this cmdlet does not delete the associated physical image blob from the storage account.</span></span>
<span data-ttu-id="418d1-108">若要刪除關聯的虛擬硬碟 (VHD) ，請使用 **DeleteVHD** 參數。</span><span class="sxs-lookup"><span data-stu-id="418d1-108">To delete the associated virtual hard drive (VHD), use the **DeleteVHD** parameter.</span></span>

## <span data-ttu-id="418d1-109">示例</span><span class="sxs-lookup"><span data-stu-id="418d1-109">EXAMPLES</span></span>

### <span data-ttu-id="418d1-110">範例1：從影像存放庫移除影像</span><span class="sxs-lookup"><span data-stu-id="418d1-110">Example 1: Remove an image from the image repository</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName "Image001"
```

<span data-ttu-id="418d1-111">這個命令會從影像存放庫中移除名為 Image001 的影像。</span><span class="sxs-lookup"><span data-stu-id="418d1-111">This command removes the image named Image001 from the image repository.</span></span>

### <span data-ttu-id="418d1-112">範例2：從影像存放庫及 VHD 中移除影像</span><span class="sxs-lookup"><span data-stu-id="418d1-112">Example 2: Remove an image from the image repository and also the VHD</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName " Image001" -DeleteVHD
```

<span data-ttu-id="418d1-113">這個命令會從影像存放庫中移除名為 Image001 的影像，同時也會從儲存空間帳戶中刪除物理 VHD 影像。</span><span class="sxs-lookup"><span data-stu-id="418d1-113">This command removes the image named Image001 from the image repository and also deletes the physical VHD image from the storage account.</span></span>

### <span data-ttu-id="418d1-114">範例3：設定訂閱內容，然後移除所有影像</span><span class="sxs-lookup"><span data-stu-id="418d1-114">Example 3: Set a subscription context and then remove all the images</span></span>
```
PS C:\> $SubsId = &amp;lt;MySubscriptionID&amp;gt;
PS C:\> $Cert = Get-AzureCertificate cert:\LocalMachine\MY\&amp;lt;CertificateThumbprint&amp;gt;
PS C:\> Get-AzureVMImage `
| Where-Object {$_.Label -match "Beta" }`
| Foreach-Object {Remove-AzureVMImage -ImageName $_.name }
```

<span data-ttu-id="418d1-115">這個命令會設定訂閱內容，然後從影像儲存庫中移除其標籤包含名稱 Beta 的所有影像。</span><span class="sxs-lookup"><span data-stu-id="418d1-115">This command sets the subscription context and then removes all the images from the image repository whose Label includes the name Beta.</span></span>

## <span data-ttu-id="418d1-116">參數</span><span class="sxs-lookup"><span data-stu-id="418d1-116">PARAMETERS</span></span>

### <span data-ttu-id="418d1-117">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="418d1-117">-DeleteVHD</span></span>
<span data-ttu-id="418d1-118">表示此 Cmdlet 會從儲存空間帳戶中刪除物理 VHD 映射 blob。</span><span class="sxs-lookup"><span data-stu-id="418d1-118">Indicates that this cmdlet deletes the physical VHD image blob from the storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="418d1-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="418d1-119">-ImageName</span></span>
<span data-ttu-id="418d1-120">指定要從影像存放庫中移除的作業系統或虛擬機器影像。</span><span class="sxs-lookup"><span data-stu-id="418d1-120">Specifies the operating system or virtual machine image to remove from the image repository.</span></span>

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

### <span data-ttu-id="418d1-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="418d1-121">-InformationAction</span></span>
<span data-ttu-id="418d1-122">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="418d1-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="418d1-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="418d1-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="418d1-124">持續</span><span class="sxs-lookup"><span data-stu-id="418d1-124">Continue</span></span>
- <span data-ttu-id="418d1-125">理會</span><span class="sxs-lookup"><span data-stu-id="418d1-125">Ignore</span></span>
- <span data-ttu-id="418d1-126">看</span><span class="sxs-lookup"><span data-stu-id="418d1-126">Inquire</span></span>
- <span data-ttu-id="418d1-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="418d1-127">SilentlyContinue</span></span>
- <span data-ttu-id="418d1-128">停止</span><span class="sxs-lookup"><span data-stu-id="418d1-128">Stop</span></span>
- <span data-ttu-id="418d1-129">封存</span><span class="sxs-lookup"><span data-stu-id="418d1-129">Suspend</span></span>

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

### <span data-ttu-id="418d1-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="418d1-130">-InformationVariable</span></span>
<span data-ttu-id="418d1-131">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="418d1-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="418d1-132">-設定檔</span><span class="sxs-lookup"><span data-stu-id="418d1-132">-Profile</span></span>
<span data-ttu-id="418d1-133">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="418d1-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="418d1-134">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="418d1-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="418d1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="418d1-135">CommonParameters</span></span>
<span data-ttu-id="418d1-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="418d1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="418d1-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="418d1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="418d1-138">輸入</span><span class="sxs-lookup"><span data-stu-id="418d1-138">INPUTS</span></span>

## <span data-ttu-id="418d1-139">輸出</span><span class="sxs-lookup"><span data-stu-id="418d1-139">OUTPUTS</span></span>

## <span data-ttu-id="418d1-140">筆記</span><span class="sxs-lookup"><span data-stu-id="418d1-140">NOTES</span></span>

## <span data-ttu-id="418d1-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="418d1-141">RELATED LINKS</span></span>

[<span data-ttu-id="418d1-142">附加 AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="418d1-142">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="418d1-143">AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="418d1-143">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="418d1-144">儲存-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="418d1-144">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="418d1-145">更新-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="418d1-145">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


