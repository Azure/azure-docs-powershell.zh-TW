---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzLogProfile.md
ms.openlocfilehash: 3c8dda7d7b84ae4ee7017c88e211b2ab5db46360
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796761"
---
# <span data-ttu-id="ca405-101">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="ca405-101">Remove-AzLogProfile</span></span>

## <span data-ttu-id="ca405-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca405-102">SYNOPSIS</span></span>
<span data-ttu-id="ca405-103">移除記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="ca405-103">Removes a log profile.</span></span>

## <span data-ttu-id="ca405-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca405-104">SYNTAX</span></span>

```
Remove-AzLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca405-105">說明</span><span class="sxs-lookup"><span data-stu-id="ca405-105">DESCRIPTION</span></span>
<span data-ttu-id="ca405-106">**AzLogProfile** Cmdlet 會移除記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="ca405-106">The **Remove-AzLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="ca405-107">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca405-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="ca405-108">示例</span><span class="sxs-lookup"><span data-stu-id="ca405-108">EXAMPLES</span></span>

## <span data-ttu-id="ca405-109">參數</span><span class="sxs-lookup"><span data-stu-id="ca405-109">PARAMETERS</span></span>

### <span data-ttu-id="ca405-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca405-110">-DefaultProfile</span></span>
<span data-ttu-id="ca405-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ca405-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca405-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="ca405-112">-Name</span></span>
<span data-ttu-id="ca405-113">指定要移除的記錄設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="ca405-113">Specifies the name of the log profile to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca405-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca405-114">-PassThru</span></span>
<span data-ttu-id="ca405-115">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="ca405-115">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca405-116">-確認</span><span class="sxs-lookup"><span data-stu-id="ca405-116">-Confirm</span></span>
<span data-ttu-id="ca405-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca405-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca405-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca405-118">-WhatIf</span></span>
<span data-ttu-id="ca405-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca405-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca405-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca405-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca405-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca405-121">CommonParameters</span></span>
<span data-ttu-id="ca405-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca405-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca405-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ca405-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca405-124">輸入</span><span class="sxs-lookup"><span data-stu-id="ca405-124">INPUTS</span></span>

### <span data-ttu-id="ca405-125">System.object</span><span class="sxs-lookup"><span data-stu-id="ca405-125">System.String</span></span>

## <span data-ttu-id="ca405-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ca405-126">OUTPUTS</span></span>

### <span data-ttu-id="ca405-127">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ca405-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="ca405-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ca405-128">NOTES</span></span>

## <span data-ttu-id="ca405-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca405-129">RELATED LINKS</span></span>

[<span data-ttu-id="ca405-130">附加 AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="ca405-130">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="ca405-131">AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="ca405-131">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)


