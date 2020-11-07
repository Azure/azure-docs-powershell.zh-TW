---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B35979E5-94C4-4DCC-B87D-D6915464CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91d464abcd8b67a0fff2cd897fa6f45fe6cb3d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967595"
---
# <span data-ttu-id="78577-101">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="78577-101">Remove-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="78577-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78577-102">SYNOPSIS</span></span>
<span data-ttu-id="78577-103">刪除 Azure RemoteApp 範本影像。</span><span class="sxs-lookup"><span data-stu-id="78577-103">Deletes an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="78577-104">句法</span><span class="sxs-lookup"><span data-stu-id="78577-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppTemplateImage [-ImageName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78577-105">說明</span><span class="sxs-lookup"><span data-stu-id="78577-105">DESCRIPTION</span></span>
<span data-ttu-id="78577-106">**AzureRemoteAppTemplateImage** Cmdlet 會刪除 Azure RemoteApp 範本影像。</span><span class="sxs-lookup"><span data-stu-id="78577-106">The **Remove-AzureRemoteAppTemplateImage** cmdlet deletes an Azure RemoteApp template image.</span></span>
<span data-ttu-id="78577-107">只有當範本圖像未連結至任何 Azure RemoteApp 集合時，才能刪除。</span><span class="sxs-lookup"><span data-stu-id="78577-107">A template image can deleted only if it is not linked to any Azure RemoteApp collection.</span></span>

## <span data-ttu-id="78577-108">示例</span><span class="sxs-lookup"><span data-stu-id="78577-108">EXAMPLES</span></span>

### <span data-ttu-id="78577-109">範例1：刪除範本圖像</span><span class="sxs-lookup"><span data-stu-id="78577-109">Example 1: Delete a template image</span></span>
```
PS C:\> Remove-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="78577-110">這個命令會刪除名為 ContosoApps 的範本影像。</span><span class="sxs-lookup"><span data-stu-id="78577-110">This command deletes the template image named ContosoApps.</span></span>

## <span data-ttu-id="78577-111">參數</span><span class="sxs-lookup"><span data-stu-id="78577-111">PARAMETERS</span></span>

### <span data-ttu-id="78577-112">-ImageName</span><span class="sxs-lookup"><span data-stu-id="78577-112">-ImageName</span></span>
<span data-ttu-id="78577-113">指定 RemoteApp 範本影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="78577-113">Specifies the name of the RemoteApp template image.</span></span>

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

### <span data-ttu-id="78577-114">-設定檔</span><span class="sxs-lookup"><span data-stu-id="78577-114">-Profile</span></span>
<span data-ttu-id="78577-115">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="78577-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="78577-116">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="78577-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="78577-117">-確認</span><span class="sxs-lookup"><span data-stu-id="78577-117">-Confirm</span></span>
<span data-ttu-id="78577-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="78577-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78577-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78577-119">-WhatIf</span></span>
<span data-ttu-id="78577-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="78577-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78577-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78577-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78577-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78577-122">CommonParameters</span></span>
<span data-ttu-id="78577-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78577-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78577-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="78577-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78577-125">輸入</span><span class="sxs-lookup"><span data-stu-id="78577-125">INPUTS</span></span>

## <span data-ttu-id="78577-126">輸出</span><span class="sxs-lookup"><span data-stu-id="78577-126">OUTPUTS</span></span>

## <span data-ttu-id="78577-127">筆記</span><span class="sxs-lookup"><span data-stu-id="78577-127">NOTES</span></span>

## <span data-ttu-id="78577-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="78577-128">RELATED LINKS</span></span>

[<span data-ttu-id="78577-129">AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="78577-129">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="78577-130">新-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="78577-130">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="78577-131">重新命名 AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="78577-131">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


