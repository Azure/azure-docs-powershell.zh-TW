---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8E67D1A4-4247-4603-8D26-42D6D48FE686
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90c654432760061d5c2ba36675c958135329b225
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967314"
---
# <span data-ttu-id="114d6-101">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="114d6-101">Remove-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="114d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="114d6-102">SYNOPSIS</span></span>
<span data-ttu-id="114d6-103">移除 Azure RemoteApp 集合。</span><span class="sxs-lookup"><span data-stu-id="114d6-103">Removes an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="114d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="114d6-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppCollection [-CollectionName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="114d6-105">說明</span><span class="sxs-lookup"><span data-stu-id="114d6-105">DESCRIPTION</span></span>
<span data-ttu-id="114d6-106">**AzureRemoteAppCollection** Cmdlet 會移除 Azure RemoteApp 集合。</span><span class="sxs-lookup"><span data-stu-id="114d6-106">The **Remove-AzureRemoteAppCollection** cmdlet removes an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="114d6-107">示例</span><span class="sxs-lookup"><span data-stu-id="114d6-107">EXAMPLES</span></span>

## <span data-ttu-id="114d6-108">參數</span><span class="sxs-lookup"><span data-stu-id="114d6-108">PARAMETERS</span></span>

### <span data-ttu-id="114d6-109">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="114d6-109">-CollectionName</span></span>
<span data-ttu-id="114d6-110">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="114d6-110">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="114d6-111">-設定檔</span><span class="sxs-lookup"><span data-stu-id="114d6-111">-Profile</span></span>
<span data-ttu-id="114d6-112">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="114d6-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="114d6-113">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="114d6-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="114d6-114">-確認</span><span class="sxs-lookup"><span data-stu-id="114d6-114">-Confirm</span></span>
<span data-ttu-id="114d6-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="114d6-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="114d6-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="114d6-116">-WhatIf</span></span>
<span data-ttu-id="114d6-117">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="114d6-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="114d6-118">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="114d6-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="114d6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="114d6-119">CommonParameters</span></span>
<span data-ttu-id="114d6-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="114d6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="114d6-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="114d6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="114d6-122">輸入</span><span class="sxs-lookup"><span data-stu-id="114d6-122">INPUTS</span></span>

## <span data-ttu-id="114d6-123">輸出</span><span class="sxs-lookup"><span data-stu-id="114d6-123">OUTPUTS</span></span>

## <span data-ttu-id="114d6-124">筆記</span><span class="sxs-lookup"><span data-stu-id="114d6-124">NOTES</span></span>

## <span data-ttu-id="114d6-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="114d6-125">RELATED LINKS</span></span>

[<span data-ttu-id="114d6-126">AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="114d6-126">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="114d6-127">新-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="114d6-127">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="114d6-128">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="114d6-128">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="114d6-129">更新-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="114d6-129">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


