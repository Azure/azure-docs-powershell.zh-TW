---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DBC4A0B8-A34A-47AC-930B-EFE23A95A216
online version: ''
schema: 2.0.0
ms.openlocfilehash: 178349299767eefb1d89c31a0199f53373bd2ae2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967441"
---
# <span data-ttu-id="1ca35-101">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="1ca35-101">New-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="1ca35-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ca35-102">SYNOPSIS</span></span>
<span data-ttu-id="1ca35-103">[上傳] 或 [匯入 Azure RemoteApp] 範本影像。</span><span class="sxs-lookup"><span data-stu-id="1ca35-103">Uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="1ca35-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ca35-104">SYNTAX</span></span>

### <span data-ttu-id="1ca35-105">UploadLocalVhd (預設) </span><span class="sxs-lookup"><span data-stu-id="1ca35-105">UploadLocalVhd (Default)</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> [-Path] <String> [-Resume]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1ca35-106">AzureVmUpload</span><span class="sxs-lookup"><span data-stu-id="1ca35-106">AzureVmUpload</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> -AzureVmImageName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1ca35-107">說明</span><span class="sxs-lookup"><span data-stu-id="1ca35-107">DESCRIPTION</span></span>
<span data-ttu-id="1ca35-108">**新的-AzureRemoteAppTemplateImage** Cmdlet 會上傳或匯入 Azure RemoteApp 範本影像。</span><span class="sxs-lookup"><span data-stu-id="1ca35-108">The **New-AzureRemoteAppTemplateImage** cmdlet uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="1ca35-109">示例</span><span class="sxs-lookup"><span data-stu-id="1ca35-109">EXAMPLES</span></span>

### <span data-ttu-id="1ca35-110">範例1：上傳 VHD 檔案以建立範本圖像</span><span class="sxs-lookup"><span data-stu-id="1ca35-110">Example 1: Upload a VHD file to create a template image</span></span>
```
PS C:\> New-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -Location "North Europe" -Path "C:\RemoteAppImages\ContosoApps.vhd"
```

<span data-ttu-id="1ca35-111">這個命令會上傳 C:\RemoteAppImages\ContosoApps.vhd，以在北歐洲資料中心建立名為 ContosoApps 的範本影像。</span><span class="sxs-lookup"><span data-stu-id="1ca35-111">This command uploads C:\RemoteAppImages\ContosoApps.vhd to create a template image named ContosoApps in the North Europe data center.</span></span>

## <span data-ttu-id="1ca35-112">參數</span><span class="sxs-lookup"><span data-stu-id="1ca35-112">PARAMETERS</span></span>

### <span data-ttu-id="1ca35-113">-AzureVmImageName</span><span class="sxs-lookup"><span data-stu-id="1ca35-113">-AzureVmImageName</span></span>
<span data-ttu-id="1ca35-114">指定要做為範本影像的 Azure 虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ca35-114">Specifies the name of an Azure virtual machine to use as a template image.</span></span>

```yaml
Type: String
Parameter Sets: AzureVmUpload
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ca35-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="1ca35-115">-ImageName</span></span>
<span data-ttu-id="1ca35-116">指定 Azure RemoteApp 範本影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ca35-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ca35-117">-位置</span><span class="sxs-lookup"><span data-stu-id="1ca35-117">-Location</span></span>
<span data-ttu-id="1ca35-118">指定範本圖像的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="1ca35-118">Specifies the Azure region of the template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ca35-119">-Path</span><span class="sxs-lookup"><span data-stu-id="1ca35-119">-Path</span></span>
<span data-ttu-id="1ca35-120">指定範本圖像的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="1ca35-120">Specifies the file path of the template image.</span></span>

```yaml
Type: String
Parameter Sets: UploadLocalVhd
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ca35-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1ca35-121">-Profile</span></span>
<span data-ttu-id="1ca35-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1ca35-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1ca35-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="1ca35-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1ca35-124">-簡歷</span><span class="sxs-lookup"><span data-stu-id="1ca35-124">-Resume</span></span>
<span data-ttu-id="1ca35-125">表示當範本影像的上傳中斷時，這個 Cmdlet 會繼續。</span><span class="sxs-lookup"><span data-stu-id="1ca35-125">Indicates that this cmdlet resumes if the upload of a template image is interrupted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UploadLocalVhd
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ca35-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ca35-126">CommonParameters</span></span>
<span data-ttu-id="1ca35-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ca35-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ca35-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1ca35-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ca35-129">輸入</span><span class="sxs-lookup"><span data-stu-id="1ca35-129">INPUTS</span></span>

## <span data-ttu-id="1ca35-130">輸出</span><span class="sxs-lookup"><span data-stu-id="1ca35-130">OUTPUTS</span></span>

## <span data-ttu-id="1ca35-131">筆記</span><span class="sxs-lookup"><span data-stu-id="1ca35-131">NOTES</span></span>

## <span data-ttu-id="1ca35-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ca35-132">RELATED LINKS</span></span>

[<span data-ttu-id="1ca35-133">AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="1ca35-133">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="1ca35-134">移除-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="1ca35-134">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="1ca35-135">重新命名 AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="1ca35-135">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


