---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: da881ceac74810b05385b26f54b7c498c60c2e77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910918"
---
# <span data-ttu-id="9030f-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9030f-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="9030f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9030f-102">SYNOPSIS</span></span>
<span data-ttu-id="9030f-103">會取回有效的租使用者 SQL 資訊保護政策。</span><span class="sxs-lookup"><span data-stu-id="9030f-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="9030f-104">語法</span><span class="sxs-lookup"><span data-stu-id="9030f-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9030f-105">描述</span><span class="sxs-lookup"><span data-stu-id="9030f-105">DESCRIPTION</span></span>
<span data-ttu-id="9030f-106">會取回有效的租使用者 SQL 資訊保護政策。</span><span class="sxs-lookup"><span data-stu-id="9030f-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="9030f-107">例子</span><span class="sxs-lookup"><span data-stu-id="9030f-107">EXAMPLES</span></span>

### <span data-ttu-id="9030f-108">例子</span><span class="sxs-lookup"><span data-stu-id="9030f-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="9030f-109">參數</span><span class="sxs-lookup"><span data-stu-id="9030f-109">PARAMETERS</span></span>

### <span data-ttu-id="9030f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9030f-110">-AsJob</span></span>
<span data-ttu-id="9030f-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9030f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9030f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9030f-112">-DefaultProfile</span></span>
<span data-ttu-id="9030f-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9030f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9030f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9030f-114">CommonParameters</span></span>
<span data-ttu-id="9030f-115">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9030f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9030f-116">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9030f-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9030f-117">輸入</span><span class="sxs-lookup"><span data-stu-id="9030f-117">INPUTS</span></span>

### <span data-ttu-id="9030f-118">System.string</span><span class="sxs-lookup"><span data-stu-id="9030f-118">System.string</span></span>

## <span data-ttu-id="9030f-119">輸出</span><span class="sxs-lookup"><span data-stu-id="9030f-119">OUTPUTS</span></span>

### <span data-ttu-id="9030f-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9030f-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="9030f-121">筆記</span><span class="sxs-lookup"><span data-stu-id="9030f-121">NOTES</span></span>

## <span data-ttu-id="9030f-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="9030f-122">RELATED LINKS</span></span>
