---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137643"
---
# <span data-ttu-id="1b3f1-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1b3f1-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="1b3f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b3f1-102">SYNOPSIS</span></span>
<span data-ttu-id="1b3f1-103">檢索有效的租使用者 SQL 資訊保護原則。</span><span class="sxs-lookup"><span data-stu-id="1b3f1-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="1b3f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b3f1-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b3f1-105">說明</span><span class="sxs-lookup"><span data-stu-id="1b3f1-105">DESCRIPTION</span></span>
<span data-ttu-id="1b3f1-106">檢索有效的租使用者 SQL 資訊保護原則。</span><span class="sxs-lookup"><span data-stu-id="1b3f1-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="1b3f1-107">示例</span><span class="sxs-lookup"><span data-stu-id="1b3f1-107">EXAMPLES</span></span>

### <span data-ttu-id="1b3f1-108">範例</span><span class="sxs-lookup"><span data-stu-id="1b3f1-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="1b3f1-109">參數</span><span class="sxs-lookup"><span data-stu-id="1b3f1-109">PARAMETERS</span></span>

### <span data-ttu-id="1b3f1-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b3f1-110">-AsJob</span></span>
<span data-ttu-id="1b3f1-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1b3f1-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b3f1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b3f1-112">-DefaultProfile</span></span>
<span data-ttu-id="1b3f1-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b3f1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b3f1-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b3f1-114">CommonParameters</span></span>
<span data-ttu-id="1b3f1-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b3f1-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b3f1-116">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1b3f1-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b3f1-117">輸入</span><span class="sxs-lookup"><span data-stu-id="1b3f1-117">INPUTS</span></span>

### <span data-ttu-id="1b3f1-118">System.object</span><span class="sxs-lookup"><span data-stu-id="1b3f1-118">System.string</span></span>

## <span data-ttu-id="1b3f1-119">輸出</span><span class="sxs-lookup"><span data-stu-id="1b3f1-119">OUTPUTS</span></span>

### <span data-ttu-id="1b3f1-120">SecurityCenter SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy （）</span><span class="sxs-lookup"><span data-stu-id="1b3f1-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="1b3f1-121">筆記</span><span class="sxs-lookup"><span data-stu-id="1b3f1-121">NOTES</span></span>

## <span data-ttu-id="1b3f1-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b3f1-122">RELATED LINKS</span></span>