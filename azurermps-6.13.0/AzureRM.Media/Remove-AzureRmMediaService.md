---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/remove-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
ms.openlocfilehash: 9ddf8291d5f6276126cea82305bbc554d05ca006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455236"
---
# <span data-ttu-id="a080b-101">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="a080b-101">Remove-AzureRmMediaService</span></span>

## <span data-ttu-id="a080b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a080b-102">SYNOPSIS</span></span>
<span data-ttu-id="a080b-103">移除媒體服務。</span><span class="sxs-lookup"><span data-stu-id="a080b-103">Removes a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a080b-104">句法</span><span class="sxs-lookup"><span data-stu-id="a080b-104">SYNTAX</span></span>

```
Remove-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a080b-105">說明</span><span class="sxs-lookup"><span data-stu-id="a080b-105">DESCRIPTION</span></span>
<span data-ttu-id="a080b-106">**AzureRmMediaService** Cmdlet 會移除媒體服務。</span><span class="sxs-lookup"><span data-stu-id="a080b-106">The **Remove-AzureRmMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="a080b-107">示例</span><span class="sxs-lookup"><span data-stu-id="a080b-107">EXAMPLES</span></span>

### <span data-ttu-id="a080b-108">範例1：移除媒體服務</span><span class="sxs-lookup"><span data-stu-id="a080b-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzureRmMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="a080b-109">這個命令會在名為 ResourceGroup001 的資源群組中，移除名為 MediaService0011 的媒體服務。</span><span class="sxs-lookup"><span data-stu-id="a080b-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="a080b-110">參數</span><span class="sxs-lookup"><span data-stu-id="a080b-110">PARAMETERS</span></span>

### <span data-ttu-id="a080b-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a080b-111">-AccountName</span></span>
<span data-ttu-id="a080b-112">指定此 Cmdlet 移除的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="a080b-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a080b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a080b-113">-DefaultProfile</span></span>
<span data-ttu-id="a080b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a080b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a080b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a080b-115">-Force</span></span>
<span data-ttu-id="a080b-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a080b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a080b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a080b-117">-ResourceGroupName</span></span>
<span data-ttu-id="a080b-118">指定包含媒體服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a080b-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="a080b-119">-確認</span><span class="sxs-lookup"><span data-stu-id="a080b-119">-Confirm</span></span>
<span data-ttu-id="a080b-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a080b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a080b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a080b-121">-WhatIf</span></span>
<span data-ttu-id="a080b-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a080b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a080b-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a080b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a080b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a080b-124">CommonParameters</span></span>
<span data-ttu-id="a080b-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a080b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a080b-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a080b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a080b-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a080b-127">INPUTS</span></span>

### <span data-ttu-id="a080b-128">System.object</span><span class="sxs-lookup"><span data-stu-id="a080b-128">System.String</span></span>

## <span data-ttu-id="a080b-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a080b-129">OUTPUTS</span></span>

### <span data-ttu-id="a080b-130">System.object</span><span class="sxs-lookup"><span data-stu-id="a080b-130">System.Boolean</span></span>

## <span data-ttu-id="a080b-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a080b-131">NOTES</span></span>

## <span data-ttu-id="a080b-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a080b-132">RELATED LINKS</span></span>

[<span data-ttu-id="a080b-133">AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="a080b-133">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="a080b-134">新-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="a080b-134">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="a080b-135">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="a080b-135">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


