---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6E369BDF-AE3C-416B-81B7-097C20147CBE
online version: ''
schema: 2.0.0
ms.openlocfilehash: bb48f7412c957ceefb7df03d79e57ce8e75447d5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967576"
---
# <span data-ttu-id="7096e-101">Remove-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="7096e-101">Remove-AzureSBNamespace</span></span>

## <span data-ttu-id="7096e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7096e-102">SYNOPSIS</span></span>
<span data-ttu-id="7096e-103">移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="7096e-103">Removes a namespace.</span></span>

## <span data-ttu-id="7096e-104">句法</span><span class="sxs-lookup"><span data-stu-id="7096e-104">SYNTAX</span></span>

```
Remove-AzureSBNamespace -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7096e-105">說明</span><span class="sxs-lookup"><span data-stu-id="7096e-105">DESCRIPTION</span></span>
<span data-ttu-id="7096e-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7096e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7096e-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="7096e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7096e-108">**AzureSBNamespace** Cmdlet 會移除服務匯流排的服務命名空間。</span><span class="sxs-lookup"><span data-stu-id="7096e-108">The **Remove-AzureSBNamespace** cmdlet removes a service namespace for Service Bus.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="7096e-109">示例</span><span class="sxs-lookup"><span data-stu-id="7096e-109">EXAMPLES</span></span>

## <span data-ttu-id="7096e-110">參數</span><span class="sxs-lookup"><span data-stu-id="7096e-110">PARAMETERS</span></span>

### <span data-ttu-id="7096e-111">-Force</span><span class="sxs-lookup"><span data-stu-id="7096e-111">-Force</span></span>
<span data-ttu-id="7096e-112">如果已啟用，則移除命名空間但不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7096e-112">If enabled, removes the namespace without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7096e-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="7096e-113">-Name</span></span>
<span data-ttu-id="7096e-114">指定要移除的命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="7096e-114">Specifies the name of the namespace to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7096e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7096e-115">-PassThru</span></span>
<span data-ttu-id="7096e-116">使此操作在成功時傳回 true。</span><span class="sxs-lookup"><span data-stu-id="7096e-116">Causes the operation to return true if it succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7096e-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="7096e-117">-Profile</span></span>
<span data-ttu-id="7096e-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7096e-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7096e-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="7096e-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7096e-120">-確認</span><span class="sxs-lookup"><span data-stu-id="7096e-120">-Confirm</span></span>
<span data-ttu-id="7096e-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7096e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7096e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7096e-122">-WhatIf</span></span>
<span data-ttu-id="7096e-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7096e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7096e-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7096e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7096e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7096e-125">CommonParameters</span></span>
<span data-ttu-id="7096e-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7096e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7096e-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7096e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7096e-128">輸入</span><span class="sxs-lookup"><span data-stu-id="7096e-128">INPUTS</span></span>

## <span data-ttu-id="7096e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="7096e-129">OUTPUTS</span></span>

## <span data-ttu-id="7096e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="7096e-130">NOTES</span></span>

## <span data-ttu-id="7096e-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="7096e-131">RELATED LINKS</span></span>

[<span data-ttu-id="7096e-132">新-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="7096e-132">New-AzureSBNamespace</span></span>](./New-AzureSBNamespace.md)


