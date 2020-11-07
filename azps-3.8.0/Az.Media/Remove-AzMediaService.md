---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: 525c5e2bfd15811e861945a6404e0b88274e2563
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965977"
---
# <span data-ttu-id="82379-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="82379-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="82379-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82379-102">SYNOPSIS</span></span>
<span data-ttu-id="82379-103">移除媒體服務。</span><span class="sxs-lookup"><span data-stu-id="82379-103">Removes a media service.</span></span>

## <span data-ttu-id="82379-104">句法</span><span class="sxs-lookup"><span data-stu-id="82379-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82379-105">說明</span><span class="sxs-lookup"><span data-stu-id="82379-105">DESCRIPTION</span></span>
<span data-ttu-id="82379-106">**AzMediaService** Cmdlet 會移除媒體服務。</span><span class="sxs-lookup"><span data-stu-id="82379-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="82379-107">示例</span><span class="sxs-lookup"><span data-stu-id="82379-107">EXAMPLES</span></span>

### <span data-ttu-id="82379-108">範例1：移除媒體服務</span><span class="sxs-lookup"><span data-stu-id="82379-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="82379-109">這個命令會在名為 ResourceGroup001 的資源群組中，移除名為 MediaService0011 的媒體服務。</span><span class="sxs-lookup"><span data-stu-id="82379-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="82379-110">參數</span><span class="sxs-lookup"><span data-stu-id="82379-110">PARAMETERS</span></span>

### <span data-ttu-id="82379-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="82379-111">-AccountName</span></span>
<span data-ttu-id="82379-112">指定此 Cmdlet 移除的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="82379-112">Specifies the name of the media service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82379-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82379-113">-DefaultProfile</span></span>
<span data-ttu-id="82379-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="82379-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82379-115">-Force</span><span class="sxs-lookup"><span data-stu-id="82379-115">-Force</span></span>
<span data-ttu-id="82379-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="82379-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="82379-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82379-117">-ResourceGroupName</span></span>
<span data-ttu-id="82379-118">指定包含媒體服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="82379-118">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82379-119">-確認</span><span class="sxs-lookup"><span data-stu-id="82379-119">-Confirm</span></span>
<span data-ttu-id="82379-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="82379-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82379-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82379-121">-WhatIf</span></span>
<span data-ttu-id="82379-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="82379-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82379-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82379-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82379-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82379-124">CommonParameters</span></span>
<span data-ttu-id="82379-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82379-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82379-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="82379-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82379-127">輸入</span><span class="sxs-lookup"><span data-stu-id="82379-127">INPUTS</span></span>

### <span data-ttu-id="82379-128">System.object</span><span class="sxs-lookup"><span data-stu-id="82379-128">System.String</span></span>

## <span data-ttu-id="82379-129">輸出</span><span class="sxs-lookup"><span data-stu-id="82379-129">OUTPUTS</span></span>

### <span data-ttu-id="82379-130">System.object</span><span class="sxs-lookup"><span data-stu-id="82379-130">System.Boolean</span></span>

## <span data-ttu-id="82379-131">筆記</span><span class="sxs-lookup"><span data-stu-id="82379-131">NOTES</span></span>

## <span data-ttu-id="82379-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="82379-132">RELATED LINKS</span></span>

[<span data-ttu-id="82379-133">AzMediaService</span><span class="sxs-lookup"><span data-stu-id="82379-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="82379-134">新-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="82379-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="82379-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="82379-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


