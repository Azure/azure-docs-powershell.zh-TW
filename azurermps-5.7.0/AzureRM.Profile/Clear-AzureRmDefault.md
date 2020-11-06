---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
ms.openlocfilehash: 4f3a463f8ae03dcbefaf9588ca196f01955070ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444459"
---
# <span data-ttu-id="5e189-101">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="5e189-101">Clear-AzureRmDefault</span></span>

## <span data-ttu-id="5e189-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e189-102">SYNOPSIS</span></span>
<span data-ttu-id="5e189-103">清除目前內容中由使用者設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="5e189-103">Clears the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e189-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e189-104">SYNTAX</span></span>

```
Clear-AzureRmDefault [-ResourceGroup] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e189-105">說明</span><span class="sxs-lookup"><span data-stu-id="5e189-105">DESCRIPTION</span></span>
<span data-ttu-id="5e189-106">Clear-AzureRmDefault Cmdlet 會根據使用者指定的切換參數，移除使用者所設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="5e189-106">The Clear-AzureRmDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="5e189-107">示例</span><span class="sxs-lookup"><span data-stu-id="5e189-107">EXAMPLES</span></span>

### <span data-ttu-id="5e189-108">範例1</span><span class="sxs-lookup"><span data-stu-id="5e189-108">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault
```

<span data-ttu-id="5e189-109">這個命令會移除使用者在目前內容中設定的所有預設值。</span><span class="sxs-lookup"><span data-stu-id="5e189-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="5e189-110">範例1</span><span class="sxs-lookup"><span data-stu-id="5e189-110">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault -ResourceGroup
```

<span data-ttu-id="5e189-111">這個命令會移除目前內容中由使用者所設定的預設資源群組。</span><span class="sxs-lookup"><span data-stu-id="5e189-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="5e189-112">參數</span><span class="sxs-lookup"><span data-stu-id="5e189-112">PARAMETERS</span></span>

### <span data-ttu-id="5e189-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e189-113">-DefaultProfile</span></span>
<span data-ttu-id="5e189-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e189-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e189-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5e189-115">-Force</span></span>
<span data-ttu-id="5e189-116">如果沒有指定預設值，則移除所有預設值</span><span class="sxs-lookup"><span data-stu-id="5e189-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="5e189-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e189-117">-PassThru</span></span>
<span data-ttu-id="5e189-118">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="5e189-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5e189-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5e189-119">-ResourceGroup</span></span>
<span data-ttu-id="5e189-120">清除預設資源群組</span><span class="sxs-lookup"><span data-stu-id="5e189-120">Clear Default Resource Group</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e189-121">-確認</span><span class="sxs-lookup"><span data-stu-id="5e189-121">-Confirm</span></span>
<span data-ttu-id="5e189-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5e189-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e189-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e189-123">-WhatIf</span></span>
<span data-ttu-id="5e189-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5e189-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e189-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5e189-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e189-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e189-126">CommonParameters</span></span>
<span data-ttu-id="5e189-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e189-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e189-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5e189-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e189-129">輸入</span><span class="sxs-lookup"><span data-stu-id="5e189-129">INPUTS</span></span>

### <span data-ttu-id="5e189-130">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="5e189-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5e189-131">輸出</span><span class="sxs-lookup"><span data-stu-id="5e189-131">OUTPUTS</span></span>

### <span data-ttu-id="5e189-132">System.object</span><span class="sxs-lookup"><span data-stu-id="5e189-132">System.Object</span></span>

## <span data-ttu-id="5e189-133">筆記</span><span class="sxs-lookup"><span data-stu-id="5e189-133">NOTES</span></span>

## <span data-ttu-id="5e189-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e189-134">RELATED LINKS</span></span>

