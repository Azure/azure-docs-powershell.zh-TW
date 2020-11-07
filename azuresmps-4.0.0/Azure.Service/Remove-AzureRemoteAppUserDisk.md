---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A4E9C9A7-7FD2-4FD5-AB35-CFF717607B44
online version: ''
schema: 2.0.0
ms.openlocfilehash: c6da222e6cbfe02e181e4a863d8ce8d585215bdd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967593"
---
# <span data-ttu-id="9a409-101">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="9a409-101">Remove-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="9a409-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a409-102">SYNOPSIS</span></span>
<span data-ttu-id="9a409-103">從 Azure RemoteApp 集合移除使用者的使用者磁片。</span><span class="sxs-lookup"><span data-stu-id="9a409-103">Removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="9a409-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a409-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUserDisk [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a409-105">說明</span><span class="sxs-lookup"><span data-stu-id="9a409-105">DESCRIPTION</span></span>
<span data-ttu-id="9a409-106">**AzureRemoteAppUserDisk** Cmdlet 會從 Azure RemoteApp 集合中移除使用者的使用者磁片。</span><span class="sxs-lookup"><span data-stu-id="9a409-106">The **Remove-AzureRemoteAppUserDisk** cmdlet removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="9a409-107">示例</span><span class="sxs-lookup"><span data-stu-id="9a409-107">EXAMPLES</span></span>

### <span data-ttu-id="9a409-108">範例1：移除使用者磁片</span><span class="sxs-lookup"><span data-stu-id="9a409-108">Example 1: Remove a user disk</span></span>
```
PS C:\> Remove-AzureRemoteAppUserDisk -CollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="9a409-109">這個命令會 PattiFuller@contoso.com 從 [集合 Contoso01] 中移除具有 UPN 的 Azure Active Directory 使用者的使用者磁片。</span><span class="sxs-lookup"><span data-stu-id="9a409-109">This command removes the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01.</span></span>

## <span data-ttu-id="9a409-110">參數</span><span class="sxs-lookup"><span data-stu-id="9a409-110">PARAMETERS</span></span>

### <span data-ttu-id="9a409-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="9a409-111">-CollectionName</span></span>
<span data-ttu-id="9a409-112">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a409-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="9a409-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9a409-113">-Profile</span></span>
<span data-ttu-id="9a409-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9a409-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9a409-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="9a409-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9a409-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="9a409-116">-UserUpn</span></span>
<span data-ttu-id="9a409-117">指定此 Cmdlet 移除磁片之使用者的使用者主要名稱 (UPN) 。</span><span class="sxs-lookup"><span data-stu-id="9a409-117">Specifies the user principal name (UPN) of the user for whom this cmdlet removes the disk.</span></span>

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

### <span data-ttu-id="9a409-118">-確認</span><span class="sxs-lookup"><span data-stu-id="9a409-118">-Confirm</span></span>
<span data-ttu-id="9a409-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9a409-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a409-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a409-120">-WhatIf</span></span>
<span data-ttu-id="9a409-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9a409-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a409-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a409-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a409-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a409-123">CommonParameters</span></span>
<span data-ttu-id="9a409-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a409-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a409-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9a409-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a409-126">輸入</span><span class="sxs-lookup"><span data-stu-id="9a409-126">INPUTS</span></span>

## <span data-ttu-id="9a409-127">輸出</span><span class="sxs-lookup"><span data-stu-id="9a409-127">OUTPUTS</span></span>

## <span data-ttu-id="9a409-128">筆記</span><span class="sxs-lookup"><span data-stu-id="9a409-128">NOTES</span></span>

## <span data-ttu-id="9a409-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a409-129">RELATED LINKS</span></span>

[<span data-ttu-id="9a409-130">複製 AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="9a409-130">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)


