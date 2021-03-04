---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 72ad39ef5b63482b10623c1945c0fb5280e07603
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910621"
---
# <span data-ttu-id="af184-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="af184-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="af184-102">簡介</span><span class="sxs-lookup"><span data-stu-id="af184-102">SYNOPSIS</span></span>
<span data-ttu-id="af184-103">設定有效的租使用者 SQL 資訊保護政策。</span><span class="sxs-lookup"><span data-stu-id="af184-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="af184-104">語法</span><span class="sxs-lookup"><span data-stu-id="af184-104">SYNTAX</span></span>

### <span data-ttu-id="af184-105">SQL 資訊保護政策 (預設) </span><span class="sxs-lookup"><span data-stu-id="af184-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af184-106">SQL 資訊保護政策檔案路徑</span><span class="sxs-lookup"><span data-stu-id="af184-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af184-107">描述</span><span class="sxs-lookup"><span data-stu-id="af184-107">DESCRIPTION</span></span>
<span data-ttu-id="af184-108">設定有效的租使用者 SQL 資訊保護政策。</span><span class="sxs-lookup"><span data-stu-id="af184-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="af184-109">例子</span><span class="sxs-lookup"><span data-stu-id="af184-109">EXAMPLES</span></span>

### <span data-ttu-id="af184-110">例子</span><span class="sxs-lookup"><span data-stu-id="af184-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="af184-111">參數</span><span class="sxs-lookup"><span data-stu-id="af184-111">PARAMETERS</span></span>

### <span data-ttu-id="af184-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af184-112">-AsJob</span></span>
<span data-ttu-id="af184-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="af184-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af184-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af184-114">-DefaultProfile</span></span>
<span data-ttu-id="af184-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="af184-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af184-116">-FilePath</span><span class="sxs-lookup"><span data-stu-id="af184-116">-FilePath</span></span>
<span data-ttu-id="af184-117">指定包含 SQL 資訊保護原則定義的 .json 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="af184-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy File Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af184-118">-策略</span><span class="sxs-lookup"><span data-stu-id="af184-118">-Policy</span></span>
<span data-ttu-id="af184-119">指定 SQL 資訊保護政策定義。</span><span class="sxs-lookup"><span data-stu-id="af184-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="af184-120">您可以指定 .json 檔案的路徑或定義該策略的 JSON 格式字串。</span><span class="sxs-lookup"><span data-stu-id="af184-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af184-121">-確認</span><span class="sxs-lookup"><span data-stu-id="af184-121">-Confirm</span></span>
<span data-ttu-id="af184-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="af184-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af184-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af184-123">-WhatIf</span></span>
<span data-ttu-id="af184-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="af184-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af184-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af184-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af184-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af184-126">CommonParameters</span></span>
<span data-ttu-id="af184-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="af184-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af184-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af184-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af184-129">輸入</span><span class="sxs-lookup"><span data-stu-id="af184-129">INPUTS</span></span>

### <span data-ttu-id="af184-130">System.String</span><span class="sxs-lookup"><span data-stu-id="af184-130">System.String</span></span>

## <span data-ttu-id="af184-131">輸出</span><span class="sxs-lookup"><span data-stu-id="af184-131">OUTPUTS</span></span>

### <span data-ttu-id="af184-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="af184-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="af184-133">筆記</span><span class="sxs-lookup"><span data-stu-id="af184-133">NOTES</span></span>

## <span data-ttu-id="af184-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="af184-134">RELATED LINKS</span></span>
