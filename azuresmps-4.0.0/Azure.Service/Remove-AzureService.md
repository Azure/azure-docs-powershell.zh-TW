---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03107EA1-6ADA-4A3E-B8E1-88788E5F3F37
online version: ''
schema: 2.0.0
ms.openlocfilehash: 21892d129319977897a6855933e3e8542460a4a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967573"
---
# <span data-ttu-id="e5c0e-101">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="e5c0e-101">Remove-AzureService</span></span>

## <span data-ttu-id="e5c0e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c0e-103">移除目前的雲端服務。</span><span class="sxs-lookup"><span data-stu-id="e5c0e-103">Removes the current cloud service.</span></span>

## <span data-ttu-id="e5c0e-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5c0e-104">SYNTAX</span></span>

```
Remove-AzureService [-ServiceName <String>] [-Force] [-PassThru] [-DeleteAll] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5c0e-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5c0e-105">DESCRIPTION</span></span>
<span data-ttu-id="e5c0e-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c0e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e5c0e-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="e5c0e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e5c0e-108">**AzureService** Cmdlet 會停止並移除目前的雲端服務，或符合指定服務和訂閱名稱的服務。</span><span class="sxs-lookup"><span data-stu-id="e5c0e-108">The **Remove-AzureService** cmdlet stops and removes the current cloud service, or the service matching the specified service and subscription name.</span></span>

## <span data-ttu-id="e5c0e-109">示例</span><span class="sxs-lookup"><span data-stu-id="e5c0e-109">EXAMPLES</span></span>

## <span data-ttu-id="e5c0e-110">參數</span><span class="sxs-lookup"><span data-stu-id="e5c0e-110">PARAMETERS</span></span>

### <span data-ttu-id="e5c0e-111">-DeleteAll</span><span class="sxs-lookup"><span data-stu-id="e5c0e-111">-DeleteAll</span></span>
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

### <span data-ttu-id="e5c0e-112">-Force</span><span class="sxs-lookup"><span data-stu-id="e5c0e-112">-Force</span></span>
<span data-ttu-id="e5c0e-113">移除服務而不提示確認。</span><span class="sxs-lookup"><span data-stu-id="e5c0e-113">Removes the service without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e5c0e-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5c0e-114">-PassThru</span></span>
<span data-ttu-id="e5c0e-115">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e5c0e-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e5c0e-116">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e5c0e-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e5c0e-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e5c0e-117">-Profile</span></span>
<span data-ttu-id="e5c0e-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e5c0e-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e5c0e-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e5c0e-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e5c0e-120">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e5c0e-120">-ServiceName</span></span>
<span data-ttu-id="e5c0e-121">指定要移除的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c0e-121">Specifies the name of the service to be removed.</span></span>
<span data-ttu-id="e5c0e-122">如果命令是從服務目錄執行，但未指定名稱，則使用目前的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="e5c0e-122">If the command is run from a service directory and no name is specified, uses the current service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c0e-123">-確認</span><span class="sxs-lookup"><span data-stu-id="e5c0e-123">-Confirm</span></span>
<span data-ttu-id="e5c0e-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5c0e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5c0e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5c0e-125">-WhatIf</span></span>
<span data-ttu-id="e5c0e-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5c0e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5c0e-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5c0e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5c0e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c0e-128">CommonParameters</span></span>
<span data-ttu-id="e5c0e-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5c0e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c0e-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5c0e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c0e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e5c0e-131">INPUTS</span></span>

## <span data-ttu-id="e5c0e-132">輸出</span><span class="sxs-lookup"><span data-stu-id="e5c0e-132">OUTPUTS</span></span>

## <span data-ttu-id="e5c0e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="e5c0e-133">NOTES</span></span>

## <span data-ttu-id="e5c0e-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5c0e-134">RELATED LINKS</span></span>

[<span data-ttu-id="e5c0e-135">發佈-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="e5c0e-135">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="e5c0e-136">停止 AzureService</span><span class="sxs-lookup"><span data-stu-id="e5c0e-136">Stop-AzureService</span></span>](./Stop-AzureService.md)

[<span data-ttu-id="e5c0e-137">開始-AzureService</span><span class="sxs-lookup"><span data-stu-id="e5c0e-137">Start-AzureService</span></span>](./Start-AzureService.md)


