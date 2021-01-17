---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 3b433860cda56f827bb58bc135240da41b89ef93
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448604"
---
# <span data-ttu-id="7622c-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7622c-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="7622c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7622c-102">SYNOPSIS</span></span>
<span data-ttu-id="7622c-103">設定有效的租使用者 SQL 資訊保護原則。</span><span class="sxs-lookup"><span data-stu-id="7622c-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="7622c-104">句法</span><span class="sxs-lookup"><span data-stu-id="7622c-104">SYNTAX</span></span>

### <span data-ttu-id="7622c-105">SQL 資訊保護原則 (預設) </span><span class="sxs-lookup"><span data-stu-id="7622c-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7622c-106">SQL 資訊保護原則檔路徑</span><span class="sxs-lookup"><span data-stu-id="7622c-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7622c-107">說明</span><span class="sxs-lookup"><span data-stu-id="7622c-107">DESCRIPTION</span></span>
<span data-ttu-id="7622c-108">設定有效的租使用者 SQL 資訊保護原則。</span><span class="sxs-lookup"><span data-stu-id="7622c-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="7622c-109">示例</span><span class="sxs-lookup"><span data-stu-id="7622c-109">EXAMPLES</span></span>

### <span data-ttu-id="7622c-110">範例</span><span class="sxs-lookup"><span data-stu-id="7622c-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="7622c-111">參數</span><span class="sxs-lookup"><span data-stu-id="7622c-111">PARAMETERS</span></span>

### <span data-ttu-id="7622c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7622c-112">-AsJob</span></span>
<span data-ttu-id="7622c-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7622c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7622c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7622c-114">-DefaultProfile</span></span>
<span data-ttu-id="7622c-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7622c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7622c-116">-FilePath</span><span class="sxs-lookup"><span data-stu-id="7622c-116">-FilePath</span></span>
<span data-ttu-id="7622c-117">指定包含 SQL 資訊保護原則定義之 json 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="7622c-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

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

### <span data-ttu-id="7622c-118">-原則</span><span class="sxs-lookup"><span data-stu-id="7622c-118">-Policy</span></span>
<span data-ttu-id="7622c-119">指定 SQL 資訊保護原則定義。</span><span class="sxs-lookup"><span data-stu-id="7622c-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="7622c-120">您可以指定 json 檔案的路徑，或是定義該原則的 JSON 格式字串。</span><span class="sxs-lookup"><span data-stu-id="7622c-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

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

### <span data-ttu-id="7622c-121">-確認</span><span class="sxs-lookup"><span data-stu-id="7622c-121">-Confirm</span></span>
<span data-ttu-id="7622c-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7622c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7622c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7622c-123">-WhatIf</span></span>
<span data-ttu-id="7622c-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7622c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7622c-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7622c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7622c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7622c-126">CommonParameters</span></span>
<span data-ttu-id="7622c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7622c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7622c-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7622c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7622c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="7622c-129">INPUTS</span></span>

### <span data-ttu-id="7622c-130">System.object</span><span class="sxs-lookup"><span data-stu-id="7622c-130">System.String</span></span>

## <span data-ttu-id="7622c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="7622c-131">OUTPUTS</span></span>

### <span data-ttu-id="7622c-132">SecurityCenter SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy （）</span><span class="sxs-lookup"><span data-stu-id="7622c-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="7622c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="7622c-133">NOTES</span></span>

## <span data-ttu-id="7622c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="7622c-134">RELATED LINKS</span></span>
