---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
ms.openlocfilehash: 1ca2244d4ed1a47535a228ed772d9d9a6ecb6acb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957163"
---
# <span data-ttu-id="ef746-101">Select-AzProfile</span><span class="sxs-lookup"><span data-stu-id="ef746-101">Select-AzProfile</span></span>

## <span data-ttu-id="ef746-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef746-102">SYNOPSIS</span></span>
<span data-ttu-id="ef746-103">針對支援多個服務設定檔的模組，請載入與指定的服務設定檔相對應的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef746-103">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="ef746-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef746-104">SYNTAX</span></span>

```
Select-AzProfile -Name <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef746-105">說明</span><span class="sxs-lookup"><span data-stu-id="ef746-105">DESCRIPTION</span></span>
<span data-ttu-id="ef746-106">針對支援多個服務設定檔的模組，請載入與指定的服務設定檔相對應的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef746-106">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="ef746-107">示例</span><span class="sxs-lookup"><span data-stu-id="ef746-107">EXAMPLES</span></span>

### <span data-ttu-id="ef746-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ef746-108">Example 1</span></span>
```powershell
PS C:\> Select-AzProfile hybrid-2019-03
```

<span data-ttu-id="ef746-109">從2019年3月載入 AzureStack 設定檔的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ef746-109">Load cmdlets for the AzureStack profile from March 2019</span></span>

## <span data-ttu-id="ef746-110">參數</span><span class="sxs-lookup"><span data-stu-id="ef746-110">PARAMETERS</span></span>

### <span data-ttu-id="ef746-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef746-111">-Name</span></span>
<span data-ttu-id="ef746-112">要選取之設定檔的名稱</span><span class="sxs-lookup"><span data-stu-id="ef746-112">The name of the profile to select</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProfileName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef746-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef746-113">-PassThru</span></span>
<span data-ttu-id="ef746-114">出現時，強迫 Cmdlet 在成功執行時傳回值</span><span class="sxs-lookup"><span data-stu-id="ef746-114">When present, forces the cmdlet to return a value on successful execution</span></span>

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

### <span data-ttu-id="ef746-115">-確認</span><span class="sxs-lookup"><span data-stu-id="ef746-115">-Confirm</span></span>
<span data-ttu-id="ef746-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ef746-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef746-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef746-117">-WhatIf</span></span>
<span data-ttu-id="ef746-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef746-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef746-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef746-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef746-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef746-120">CommonParameters</span></span>
<span data-ttu-id="ef746-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef746-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef746-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ef746-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef746-123">輸入</span><span class="sxs-lookup"><span data-stu-id="ef746-123">INPUTS</span></span>

### <span data-ttu-id="ef746-124">所有</span><span class="sxs-lookup"><span data-stu-id="ef746-124">None</span></span>

## <span data-ttu-id="ef746-125">輸出</span><span class="sxs-lookup"><span data-stu-id="ef746-125">OUTPUTS</span></span>

### <span data-ttu-id="ef746-126">System.object</span><span class="sxs-lookup"><span data-stu-id="ef746-126">System.Object</span></span>
## <span data-ttu-id="ef746-127">筆記</span><span class="sxs-lookup"><span data-stu-id="ef746-127">NOTES</span></span>

## <span data-ttu-id="ef746-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef746-128">RELATED LINKS</span></span>
