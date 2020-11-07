---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Select-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Select-AzProfile.md
ms.openlocfilehash: 04b98f15def219c269bf18f21fb371822cc97f6d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794109"
---
# <span data-ttu-id="50107-101">Select-AzProfile</span><span class="sxs-lookup"><span data-stu-id="50107-101">Select-AzProfile</span></span>

## <span data-ttu-id="50107-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50107-102">SYNOPSIS</span></span>
<span data-ttu-id="50107-103">針對支援多個服務設定檔的模組，請載入與指定的服務設定檔相對應的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50107-103">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="50107-104">句法</span><span class="sxs-lookup"><span data-stu-id="50107-104">SYNTAX</span></span>

```
Select-AzProfile -Name <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50107-105">說明</span><span class="sxs-lookup"><span data-stu-id="50107-105">DESCRIPTION</span></span>
<span data-ttu-id="50107-106">針對支援多個服務設定檔的模組，請載入與指定的服務設定檔相對應的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50107-106">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="50107-107">示例</span><span class="sxs-lookup"><span data-stu-id="50107-107">EXAMPLES</span></span>

### <span data-ttu-id="50107-108">範例1</span><span class="sxs-lookup"><span data-stu-id="50107-108">Example 1</span></span>
```powershell
PS C:\> Select-AzProfile hybrid-2019-03
```

<span data-ttu-id="50107-109">從2019年3月載入 AzureStack 設定檔的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="50107-109">Load cmdlets for the AzureStack profile from March 2019</span></span>

## <span data-ttu-id="50107-110">參數</span><span class="sxs-lookup"><span data-stu-id="50107-110">PARAMETERS</span></span>

### <span data-ttu-id="50107-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="50107-111">-Name</span></span>
<span data-ttu-id="50107-112">要選取之設定檔的名稱</span><span class="sxs-lookup"><span data-stu-id="50107-112">The name of the profile to select</span></span>

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

### <span data-ttu-id="50107-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50107-113">-PassThru</span></span>
<span data-ttu-id="50107-114">出現時，強迫 Cmdlet 在成功執行時傳回值</span><span class="sxs-lookup"><span data-stu-id="50107-114">When present, forces the cmdlet to return a value on successful execution</span></span>

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

### <span data-ttu-id="50107-115">-確認</span><span class="sxs-lookup"><span data-stu-id="50107-115">-Confirm</span></span>
<span data-ttu-id="50107-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="50107-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50107-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50107-117">-WhatIf</span></span>
<span data-ttu-id="50107-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50107-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50107-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50107-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50107-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50107-120">CommonParameters</span></span>
<span data-ttu-id="50107-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50107-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50107-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="50107-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50107-123">輸入</span><span class="sxs-lookup"><span data-stu-id="50107-123">INPUTS</span></span>

### <span data-ttu-id="50107-124">所有</span><span class="sxs-lookup"><span data-stu-id="50107-124">None</span></span>

## <span data-ttu-id="50107-125">輸出</span><span class="sxs-lookup"><span data-stu-id="50107-125">OUTPUTS</span></span>

### <span data-ttu-id="50107-126">System.object</span><span class="sxs-lookup"><span data-stu-id="50107-126">System.Object</span></span>
## <span data-ttu-id="50107-127">筆記</span><span class="sxs-lookup"><span data-stu-id="50107-127">NOTES</span></span>

## <span data-ttu-id="50107-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="50107-128">RELATED LINKS</span></span>
