---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/disable-azurermsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Disable-AzureRmSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Disable-AzureRmSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: cc38d619b810f2567594c0c1020190c271dc9f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448198"
---
# <span data-ttu-id="73611-101">Disable-AzureRmSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="73611-101">Disable-AzureRmSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="73611-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73611-102">SYNOPSIS</span></span>
<span data-ttu-id="73611-103">在伺服器上停用 [高級威脅防護]。</span><span class="sxs-lookup"><span data-stu-id="73611-103">Disables Advanced Threat Protection on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73611-104">句法</span><span class="sxs-lookup"><span data-stu-id="73611-104">SYNTAX</span></span>

```
Disable-AzureRmSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73611-105">說明</span><span class="sxs-lookup"><span data-stu-id="73611-105">DESCRIPTION</span></span>
<span data-ttu-id="73611-106">**Disable AzureRmSqlServerAdvancedThreatProtection** Cmdlet 會在伺服器上停用高級威脅防護。</span><span class="sxs-lookup"><span data-stu-id="73611-106">The **Disable-AzureRmSqlServerAdvancedThreatProtection** cmdlet disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="73611-107">示例</span><span class="sxs-lookup"><span data-stu-id="73611-107">EXAMPLES</span></span>

### <span data-ttu-id="73611-108">範例 1-停用伺服器高級威脅防護</span><span class="sxs-lookup"><span data-stu-id="73611-108">Example 1 - Disable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Disable-AzureRmSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="73611-109">範例 2-從伺服器資源停用伺服器高級威脅防護</span><span class="sxs-lookup"><span data-stu-id="73611-109">Example 2 - Disable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzureRmSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="73611-110">參數</span><span class="sxs-lookup"><span data-stu-id="73611-110">PARAMETERS</span></span>

### <span data-ttu-id="73611-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73611-111">-DefaultProfile</span></span>
<span data-ttu-id="73611-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="73611-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73611-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73611-113">-InputObject</span></span>
<span data-ttu-id="73611-114">要搭配高級威脅防護原則操作使用的伺服器物件</span><span class="sxs-lookup"><span data-stu-id="73611-114">The server object to use with Advanced Threat Protection policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73611-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73611-115">-ResourceGroupName</span></span>
<span data-ttu-id="73611-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="73611-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="73611-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="73611-117">-ServerName</span></span>
<span data-ttu-id="73611-118">SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="73611-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="73611-119">-確認</span><span class="sxs-lookup"><span data-stu-id="73611-119">-Confirm</span></span>
<span data-ttu-id="73611-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="73611-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73611-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73611-121">-WhatIf</span></span>
<span data-ttu-id="73611-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="73611-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73611-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73611-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73611-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73611-124">CommonParameters</span></span>
<span data-ttu-id="73611-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73611-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73611-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="73611-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73611-127">輸入</span><span class="sxs-lookup"><span data-stu-id="73611-127">INPUTS</span></span>

### <span data-ttu-id="73611-128">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="73611-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="73611-129">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="73611-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="73611-130">System.object</span><span class="sxs-lookup"><span data-stu-id="73611-130">System.String</span></span>

## <span data-ttu-id="73611-131">輸出</span><span class="sxs-lookup"><span data-stu-id="73611-131">OUTPUTS</span></span>

### <span data-ttu-id="73611-132">ServerAdvancedThreatProtectionPolicyModel 中的 [AdvancedThreatProtection]</span><span class="sxs-lookup"><span data-stu-id="73611-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="73611-133">筆記</span><span class="sxs-lookup"><span data-stu-id="73611-133">NOTES</span></span>

## <span data-ttu-id="73611-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="73611-134">RELATED LINKS</span></span>
