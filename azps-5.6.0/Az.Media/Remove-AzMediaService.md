---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: 5b27574dc6ea60472a16c0b647027ceba17a87b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916101"
---
# <span data-ttu-id="4b81a-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="4b81a-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="4b81a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4b81a-102">SYNOPSIS</span></span>
<span data-ttu-id="4b81a-103">移除媒體服務。</span><span class="sxs-lookup"><span data-stu-id="4b81a-103">Removes a media service.</span></span>

## <span data-ttu-id="4b81a-104">語法</span><span class="sxs-lookup"><span data-stu-id="4b81a-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b81a-105">描述</span><span class="sxs-lookup"><span data-stu-id="4b81a-105">DESCRIPTION</span></span>
<span data-ttu-id="4b81a-106">**Remove-AzMediaService** Cmdlet 會移除媒體服務。</span><span class="sxs-lookup"><span data-stu-id="4b81a-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="4b81a-107">例子</span><span class="sxs-lookup"><span data-stu-id="4b81a-107">EXAMPLES</span></span>

### <span data-ttu-id="4b81a-108">範例 1：移除媒體服務</span><span class="sxs-lookup"><span data-stu-id="4b81a-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="4b81a-109">此命令會移除名為 ResourceGroup001 的資源群組中名為 MediaService0011 的媒體服務。</span><span class="sxs-lookup"><span data-stu-id="4b81a-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="4b81a-110">參數</span><span class="sxs-lookup"><span data-stu-id="4b81a-110">PARAMETERS</span></span>

### <span data-ttu-id="4b81a-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4b81a-111">-AccountName</span></span>
<span data-ttu-id="4b81a-112">指定此 Cmdlet 移除的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="4b81a-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4b81a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b81a-113">-DefaultProfile</span></span>
<span data-ttu-id="4b81a-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="4b81a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b81a-115">-強制</span><span class="sxs-lookup"><span data-stu-id="4b81a-115">-Force</span></span>
<span data-ttu-id="4b81a-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="4b81a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4b81a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b81a-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b81a-118">指定包含媒體服務的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4b81a-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="4b81a-119">-確認</span><span class="sxs-lookup"><span data-stu-id="4b81a-119">-Confirm</span></span>
<span data-ttu-id="4b81a-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4b81a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b81a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b81a-121">-WhatIf</span></span>
<span data-ttu-id="4b81a-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4b81a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b81a-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b81a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b81a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b81a-124">CommonParameters</span></span>
<span data-ttu-id="4b81a-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4b81a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b81a-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4b81a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b81a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="4b81a-127">INPUTS</span></span>

### <span data-ttu-id="4b81a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4b81a-128">System.String</span></span>

## <span data-ttu-id="4b81a-129">輸出</span><span class="sxs-lookup"><span data-stu-id="4b81a-129">OUTPUTS</span></span>

### <span data-ttu-id="4b81a-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4b81a-130">System.Boolean</span></span>

## <span data-ttu-id="4b81a-131">筆記</span><span class="sxs-lookup"><span data-stu-id="4b81a-131">NOTES</span></span>

## <span data-ttu-id="4b81a-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b81a-132">RELATED LINKS</span></span>

[<span data-ttu-id="4b81a-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="4b81a-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="4b81a-134">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="4b81a-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="4b81a-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="4b81a-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


