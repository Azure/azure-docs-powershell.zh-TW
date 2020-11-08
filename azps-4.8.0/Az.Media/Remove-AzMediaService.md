---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: 525c5e2bfd15811e861945a6404e0b88274e2563
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970986"
---
# <span data-ttu-id="e40a3-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e40a3-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="e40a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e40a3-102">SYNOPSIS</span></span>
<span data-ttu-id="e40a3-103">移除媒體服務。</span><span class="sxs-lookup"><span data-stu-id="e40a3-103">Removes a media service.</span></span>

## <span data-ttu-id="e40a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="e40a3-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e40a3-105">說明</span><span class="sxs-lookup"><span data-stu-id="e40a3-105">DESCRIPTION</span></span>
<span data-ttu-id="e40a3-106">**AzMediaService** Cmdlet 會移除媒體服務。</span><span class="sxs-lookup"><span data-stu-id="e40a3-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="e40a3-107">示例</span><span class="sxs-lookup"><span data-stu-id="e40a3-107">EXAMPLES</span></span>

### <span data-ttu-id="e40a3-108">範例1：移除媒體服務</span><span class="sxs-lookup"><span data-stu-id="e40a3-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="e40a3-109">這個命令會在名為 ResourceGroup001 的資源群組中，移除名為 MediaService0011 的媒體服務。</span><span class="sxs-lookup"><span data-stu-id="e40a3-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="e40a3-110">參數</span><span class="sxs-lookup"><span data-stu-id="e40a3-110">PARAMETERS</span></span>

### <span data-ttu-id="e40a3-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e40a3-111">-AccountName</span></span>
<span data-ttu-id="e40a3-112">指定此 Cmdlet 移除的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="e40a3-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e40a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e40a3-113">-DefaultProfile</span></span>
<span data-ttu-id="e40a3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e40a3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e40a3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e40a3-115">-Force</span></span>
<span data-ttu-id="e40a3-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e40a3-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e40a3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e40a3-117">-ResourceGroupName</span></span>
<span data-ttu-id="e40a3-118">指定包含媒體服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e40a3-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="e40a3-119">-確認</span><span class="sxs-lookup"><span data-stu-id="e40a3-119">-Confirm</span></span>
<span data-ttu-id="e40a3-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e40a3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e40a3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e40a3-121">-WhatIf</span></span>
<span data-ttu-id="e40a3-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e40a3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e40a3-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e40a3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e40a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e40a3-124">CommonParameters</span></span>
<span data-ttu-id="e40a3-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e40a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e40a3-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e40a3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e40a3-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e40a3-127">INPUTS</span></span>

### <span data-ttu-id="e40a3-128">System.object</span><span class="sxs-lookup"><span data-stu-id="e40a3-128">System.String</span></span>

## <span data-ttu-id="e40a3-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e40a3-129">OUTPUTS</span></span>

### <span data-ttu-id="e40a3-130">System.object</span><span class="sxs-lookup"><span data-stu-id="e40a3-130">System.Boolean</span></span>

## <span data-ttu-id="e40a3-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e40a3-131">NOTES</span></span>

## <span data-ttu-id="e40a3-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e40a3-132">RELATED LINKS</span></span>

[<span data-ttu-id="e40a3-133">AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e40a3-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="e40a3-134">新-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e40a3-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="e40a3-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e40a3-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


