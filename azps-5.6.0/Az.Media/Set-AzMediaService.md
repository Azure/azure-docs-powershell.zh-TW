---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/powershell/module/az.media/set-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
ms.openlocfilehash: 410b1c87832b4debdfd50cbe6adf27326f12a303
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909670"
---
# <span data-ttu-id="37615-101">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="37615-101">Set-AzMediaService</span></span>

## <span data-ttu-id="37615-102">簡介</span><span class="sxs-lookup"><span data-stu-id="37615-102">SYNOPSIS</span></span>
<span data-ttu-id="37615-103">修改現有媒體服務的指定屬性。</span><span class="sxs-lookup"><span data-stu-id="37615-103">Modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="37615-104">語法</span><span class="sxs-lookup"><span data-stu-id="37615-104">SYNTAX</span></span>

```
Set-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37615-105">描述</span><span class="sxs-lookup"><span data-stu-id="37615-105">DESCRIPTION</span></span>
<span data-ttu-id="37615-106">**Set-AzMediaService** Cmdlet 會修改現有媒體服務的指定屬性。</span><span class="sxs-lookup"><span data-stu-id="37615-106">The **Set-AzMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="37615-107">例子</span><span class="sxs-lookup"><span data-stu-id="37615-107">EXAMPLES</span></span>

### <span data-ttu-id="37615-108">範例 1：修改現有的媒體服務</span><span class="sxs-lookup"><span data-stu-id="37615-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tag $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="37615-109">第一個命令會建立一系列標記，並儲存在名為 $Tags 的變數中。</span><span class="sxs-lookup"><span data-stu-id="37615-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="37615-110">第二個命令會更新名為 MediaService001 的媒體服務，這項服務屬於名為 ResourceGroup123 的資源群組，其標記會儲存在 $Tags 變數中。</span><span class="sxs-lookup"><span data-stu-id="37615-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="37615-111">該命令也會使用儲存在變數中的儲存$StorageAccounts陣列。</span><span class="sxs-lookup"><span data-stu-id="37615-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="37615-112">參數</span><span class="sxs-lookup"><span data-stu-id="37615-112">PARAMETERS</span></span>

### <span data-ttu-id="37615-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="37615-113">-AccountName</span></span>
<span data-ttu-id="37615-114">指定此 Cmdlet 修改的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="37615-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="37615-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37615-115">-DefaultProfile</span></span>
<span data-ttu-id="37615-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="37615-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37615-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37615-117">-ResourceGroupName</span></span>
<span data-ttu-id="37615-118">指定包含媒體服務的資源組名。</span><span class="sxs-lookup"><span data-stu-id="37615-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="37615-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="37615-119">-StorageAccounts</span></span>
<span data-ttu-id="37615-120">指定此 Cmdlet 與媒體服務建立關聯之儲存空間帳戶的陣列。</span><span class="sxs-lookup"><span data-stu-id="37615-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37615-121">-標記</span><span class="sxs-lookup"><span data-stu-id="37615-121">-Tag</span></span>
<span data-ttu-id="37615-122">與媒體帳戶相關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="37615-122">The tags associated with the media account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37615-123">-確認</span><span class="sxs-lookup"><span data-stu-id="37615-123">-Confirm</span></span>
<span data-ttu-id="37615-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="37615-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37615-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37615-125">-WhatIf</span></span>
<span data-ttu-id="37615-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="37615-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37615-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37615-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37615-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37615-128">CommonParameters</span></span>
<span data-ttu-id="37615-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="37615-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37615-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="37615-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37615-131">輸入</span><span class="sxs-lookup"><span data-stu-id="37615-131">INPUTS</span></span>

### <span data-ttu-id="37615-132">System.String</span><span class="sxs-lookup"><span data-stu-id="37615-132">System.String</span></span>

### <span data-ttu-id="37615-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="37615-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="37615-134">Microsoft.Azure.Commands.Media.models.PSStorageAccount[]</span><span class="sxs-lookup"><span data-stu-id="37615-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="37615-135">輸出</span><span class="sxs-lookup"><span data-stu-id="37615-135">OUTPUTS</span></span>

### <span data-ttu-id="37615-136">Microsoft.Azure.Commands.Media.models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="37615-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="37615-137">筆記</span><span class="sxs-lookup"><span data-stu-id="37615-137">NOTES</span></span>

## <span data-ttu-id="37615-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="37615-138">RELATED LINKS</span></span>

[<span data-ttu-id="37615-139">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="37615-139">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="37615-140">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="37615-140">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="37615-141">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="37615-141">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)


