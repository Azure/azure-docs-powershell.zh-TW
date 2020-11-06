---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: 735ea22547183b8047a3a32d0a147b428b39f630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454131"
---
# <span data-ttu-id="1e73c-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="1e73c-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="1e73c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e73c-102">SYNOPSIS</span></span>
<span data-ttu-id="1e73c-103">刪除 active directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="1e73c-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e73c-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e73c-104">SYNTAX</span></span>

```
Remove-AzureRmADUser -UPNOrObjectId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e73c-105">說明</span><span class="sxs-lookup"><span data-stu-id="1e73c-105">DESCRIPTION</span></span>
<span data-ttu-id="1e73c-106">刪除 active directory 使用者 (公司/學校帳戶也會 popularly 稱為組織識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="1e73c-106">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="1e73c-107">示例</span><span class="sxs-lookup"><span data-stu-id="1e73c-107">EXAMPLES</span></span>

### <span data-ttu-id="1e73c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1e73c-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1e73c-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="1e73c-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="1e73c-110">參數</span><span class="sxs-lookup"><span data-stu-id="1e73c-110">PARAMETERS</span></span>

### <span data-ttu-id="1e73c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e73c-111">-DefaultProfile</span></span>
<span data-ttu-id="1e73c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1e73c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e73c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1e73c-113">-Force</span></span>
<span data-ttu-id="1e73c-114">如果已指定，就不要求確認刪除使用者。</span><span class="sxs-lookup"><span data-stu-id="1e73c-114">If specified, doesn't ask for confirmation for deleting user.</span></span>

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

### <span data-ttu-id="1e73c-115">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="1e73c-115">-UPNOrObjectId</span></span>
<span data-ttu-id="1e73c-116">要刪除之使用者的使用者主要名稱或 objectId。</span><span class="sxs-lookup"><span data-stu-id="1e73c-116">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="1e73c-117">-確認</span><span class="sxs-lookup"><span data-stu-id="1e73c-117">-Confirm</span></span>
<span data-ttu-id="1e73c-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1e73c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e73c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e73c-119">-WhatIf</span></span>
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

### <span data-ttu-id="1e73c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e73c-120">CommonParameters</span></span>
<span data-ttu-id="1e73c-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e73c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e73c-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e73c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e73c-123">輸入</span><span class="sxs-lookup"><span data-stu-id="1e73c-123">INPUTS</span></span>

### <span data-ttu-id="1e73c-124">所有</span><span class="sxs-lookup"><span data-stu-id="1e73c-124">None</span></span>
<span data-ttu-id="1e73c-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="1e73c-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1e73c-126">輸出</span><span class="sxs-lookup"><span data-stu-id="1e73c-126">OUTPUTS</span></span>

## <span data-ttu-id="1e73c-127">筆記</span><span class="sxs-lookup"><span data-stu-id="1e73c-127">NOTES</span></span>

## <span data-ttu-id="1e73c-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e73c-128">RELATED LINKS</span></span>

[<span data-ttu-id="1e73c-129">新-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="1e73c-129">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="1e73c-130">AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="1e73c-130">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="1e73c-131">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="1e73c-131">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

