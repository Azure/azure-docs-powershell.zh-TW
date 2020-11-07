---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DB3F85D6-5962-4288-AD75-0C30448B769C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88438fa66e39b5ad63db7b6d2609107d224f7faf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967466"
---
# <span data-ttu-id="a1e3c-101">Unpublish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="a1e3c-101">Unpublish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="a1e3c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1e3c-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e3c-103">Unpublishes Azure RemoteApp 程式。</span><span class="sxs-lookup"><span data-stu-id="a1e3c-103">Unpublishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="a1e3c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1e3c-104">SYNTAX</span></span>

```
Unpublish-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String[]>] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1e3c-105">說明</span><span class="sxs-lookup"><span data-stu-id="a1e3c-105">DESCRIPTION</span></span>
<span data-ttu-id="a1e3c-106">**AzureRemoteAppProgram** Cmdlet Unpublishes Azure RemoteApp 程式。</span><span class="sxs-lookup"><span data-stu-id="a1e3c-106">The **Unpublish-AzureRemoteAppProgram** cmdlet unpublishes an Azure RemoteApp program.</span></span>
<span data-ttu-id="a1e3c-107">在您取消發佈程式之後，Azure RemoteApp 集合的使用者就無法再使用它。</span><span class="sxs-lookup"><span data-stu-id="a1e3c-107">After you unpublish a program, it is no longer available to the users of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="a1e3c-108">示例</span><span class="sxs-lookup"><span data-stu-id="a1e3c-108">EXAMPLES</span></span>

## <span data-ttu-id="a1e3c-109">參數</span><span class="sxs-lookup"><span data-stu-id="a1e3c-109">PARAMETERS</span></span>

### <span data-ttu-id="a1e3c-110">-別名</span><span class="sxs-lookup"><span data-stu-id="a1e3c-110">-Alias</span></span>
<span data-ttu-id="a1e3c-111">指定要取消發佈之程式的別名陣列。</span><span class="sxs-lookup"><span data-stu-id="a1e3c-111">Specifies an array of aliases of the programs to unpublish.</span></span>
<span data-ttu-id="a1e3c-112">使用 **AzureRemoteAppProgram** ，以取得要取消發佈之程式的別名。</span><span class="sxs-lookup"><span data-stu-id="a1e3c-112">Use **Get-AzureRemoteAppProgram** to retrieve the alias of a program to unpublish.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1e3c-113">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="a1e3c-113">-CollectionName</span></span>
<span data-ttu-id="a1e3c-114">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1e3c-114">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="a1e3c-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a1e3c-115">-Profile</span></span>
<span data-ttu-id="a1e3c-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a1e3c-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a1e3c-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a1e3c-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a1e3c-118">-確認</span><span class="sxs-lookup"><span data-stu-id="a1e3c-118">-Confirm</span></span>
<span data-ttu-id="a1e3c-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a1e3c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1e3c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1e3c-120">-WhatIf</span></span>
<span data-ttu-id="a1e3c-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a1e3c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1e3c-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a1e3c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1e3c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e3c-123">CommonParameters</span></span>
<span data-ttu-id="a1e3c-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1e3c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e3c-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a1e3c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e3c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a1e3c-126">INPUTS</span></span>

## <span data-ttu-id="a1e3c-127">輸出</span><span class="sxs-lookup"><span data-stu-id="a1e3c-127">OUTPUTS</span></span>

## <span data-ttu-id="a1e3c-128">筆記</span><span class="sxs-lookup"><span data-stu-id="a1e3c-128">NOTES</span></span>

## <span data-ttu-id="a1e3c-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1e3c-129">RELATED LINKS</span></span>

[<span data-ttu-id="a1e3c-130">AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="a1e3c-130">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="a1e3c-131">發佈-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="a1e3c-131">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)


