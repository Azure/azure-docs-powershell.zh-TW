---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 87163619-DEA4-4183-BB11-2D7B16F4BE8A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee4e094c1e38c54b1f9ad4e78723ec49fff1f75b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967693"
---
# <span data-ttu-id="f30c3-101">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="f30c3-101">Invoke-AzureRemoteAppSessionLogoff</span></span>

## <span data-ttu-id="f30c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f30c3-102">SYNOPSIS</span></span>
<span data-ttu-id="f30c3-103">立即登出 Azure RemoteApp 會話。</span><span class="sxs-lookup"><span data-stu-id="f30c3-103">Logs off an Azure RemoteApp session immediately.</span></span>

## <span data-ttu-id="f30c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="f30c3-104">SYNTAX</span></span>

```
Invoke-AzureRemoteAppSessionLogoff [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f30c3-105">說明</span><span class="sxs-lookup"><span data-stu-id="f30c3-105">DESCRIPTION</span></span>
<span data-ttu-id="f30c3-106">**AzureRemoteAppSessionLogoff** Cmdlet 會立即從執行于 Azure RemoteApp 的遠端會話登出使用者。</span><span class="sxs-lookup"><span data-stu-id="f30c3-106">The **Invoke-AzureRemoteAppSessionLogoff** cmdlet immediately logs off a user from a remote session running in Azure RemoteApp.</span></span>

## <span data-ttu-id="f30c3-107">示例</span><span class="sxs-lookup"><span data-stu-id="f30c3-107">EXAMPLES</span></span>

### <span data-ttu-id="f30c3-108">範例1：登出使用者</span><span class="sxs-lookup"><span data-stu-id="f30c3-108">Example 1: Log off a user</span></span>
```
PS C:\> Invoke-AzureRemoteAppSessionLogoff -CollectionName ContosoApps -UserUpn PattiFuller@contoso.com
```

<span data-ttu-id="f30c3-109">這個命令會登出其 UPN 的使用者 PattiFuller@contoso.com 。</span><span class="sxs-lookup"><span data-stu-id="f30c3-109">This command logs off the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="f30c3-110">參數</span><span class="sxs-lookup"><span data-stu-id="f30c3-110">PARAMETERS</span></span>

### <span data-ttu-id="f30c3-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="f30c3-111">-CollectionName</span></span>
<span data-ttu-id="f30c3-112">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="f30c3-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="f30c3-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f30c3-113">-Profile</span></span>
<span data-ttu-id="f30c3-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f30c3-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f30c3-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f30c3-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f30c3-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="f30c3-116">-UserUpn</span></span>
<span data-ttu-id="f30c3-117">Specifes 使用者的使用者主要名稱 (UPN) ，例如 PattiFuller@contoso.com 。</span><span class="sxs-lookup"><span data-stu-id="f30c3-117">Specifes the user Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30c3-118">-確認</span><span class="sxs-lookup"><span data-stu-id="f30c3-118">-Confirm</span></span>
<span data-ttu-id="f30c3-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f30c3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f30c3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f30c3-120">-WhatIf</span></span>
<span data-ttu-id="f30c3-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f30c3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f30c3-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f30c3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f30c3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30c3-123">CommonParameters</span></span>
<span data-ttu-id="f30c3-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f30c3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30c3-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f30c3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30c3-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f30c3-126">INPUTS</span></span>

## <span data-ttu-id="f30c3-127">輸出</span><span class="sxs-lookup"><span data-stu-id="f30c3-127">OUTPUTS</span></span>

## <span data-ttu-id="f30c3-128">筆記</span><span class="sxs-lookup"><span data-stu-id="f30c3-128">NOTES</span></span>

## <span data-ttu-id="f30c3-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="f30c3-129">RELATED LINKS</span></span>

[<span data-ttu-id="f30c3-130">附加 AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="f30c3-130">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="f30c3-131">中斷連線-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="f30c3-131">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="f30c3-132">AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="f30c3-132">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)


