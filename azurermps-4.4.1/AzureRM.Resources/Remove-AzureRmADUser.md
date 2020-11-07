---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: b0f4e67630a3a762fe78c9438c6ae39f948404c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625692"
---
# <span data-ttu-id="37f3d-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="37f3d-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="37f3d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="37f3d-103">刪除 active directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="37f3d-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37f3d-104">句法</span><span class="sxs-lookup"><span data-stu-id="37f3d-104">SYNTAX</span></span>

```
Remove-AzureRmADUser -UPNOrObjectId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37f3d-105">說明</span><span class="sxs-lookup"><span data-stu-id="37f3d-105">DESCRIPTION</span></span>
<span data-ttu-id="37f3d-106">刪除 active directory 使用者 (公司/學校帳戶也會 popularly 稱為組織識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="37f3d-106">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="37f3d-107">示例</span><span class="sxs-lookup"><span data-stu-id="37f3d-107">EXAMPLES</span></span>

### <span data-ttu-id="37f3d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="37f3d-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="37f3d-109">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="37f3d-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="37f3d-110">參數</span><span class="sxs-lookup"><span data-stu-id="37f3d-110">PARAMETERS</span></span>

### <span data-ttu-id="37f3d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="37f3d-111">-Force</span></span>
<span data-ttu-id="37f3d-112">如果已指定，就不要求確認刪除使用者。</span><span class="sxs-lookup"><span data-stu-id="37f3d-112">If specified, doesn't ask for confirmation for deleting user.</span></span>

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

### <span data-ttu-id="37f3d-113">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="37f3d-113">-UPNOrObjectId</span></span>
<span data-ttu-id="37f3d-114">要刪除之使用者的使用者主要名稱或 objectId。</span><span class="sxs-lookup"><span data-stu-id="37f3d-114">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="37f3d-115">-確認</span><span class="sxs-lookup"><span data-stu-id="37f3d-115">-Confirm</span></span>
<span data-ttu-id="37f3d-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="37f3d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37f3d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37f3d-117">-WhatIf</span></span>
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

### <span data-ttu-id="37f3d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37f3d-118">-DefaultProfile</span></span>
<span data-ttu-id="37f3d-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37f3d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37f3d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37f3d-120">CommonParameters</span></span>
<span data-ttu-id="37f3d-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37f3d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37f3d-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="37f3d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37f3d-123">輸入</span><span class="sxs-lookup"><span data-stu-id="37f3d-123">INPUTS</span></span>

## <span data-ttu-id="37f3d-124">輸出</span><span class="sxs-lookup"><span data-stu-id="37f3d-124">OUTPUTS</span></span>

## <span data-ttu-id="37f3d-125">筆記</span><span class="sxs-lookup"><span data-stu-id="37f3d-125">NOTES</span></span>

## <span data-ttu-id="37f3d-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="37f3d-126">RELATED LINKS</span></span>

[<span data-ttu-id="37f3d-127">新-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="37f3d-127">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="37f3d-128">AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="37f3d-128">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="37f3d-129">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="37f3d-129">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

