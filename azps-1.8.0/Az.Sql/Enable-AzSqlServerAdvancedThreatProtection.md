---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: aaaf417137bb1ec16150a2bf3d0ac88b64e70fae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620503"
---
# <span data-ttu-id="49804-101">Enable-AzSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="49804-101">Enable-AzSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="49804-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49804-102">SYNOPSIS</span></span>
<span data-ttu-id="49804-103">在伺服器上啟用高級威脅防護。</span><span class="sxs-lookup"><span data-stu-id="49804-103">Enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="49804-104">句法</span><span class="sxs-lookup"><span data-stu-id="49804-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49804-105">說明</span><span class="sxs-lookup"><span data-stu-id="49804-105">DESCRIPTION</span></span>
<span data-ttu-id="49804-106">**Enable-AzSqlServerAdvancedThreatProtection** Cmdlet 可在伺服器上啟用高級威脅防護。</span><span class="sxs-lookup"><span data-stu-id="49804-106">The **Enable-AzSqlServerAdvancedThreatProtection** cmdlet enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="49804-107">示例</span><span class="sxs-lookup"><span data-stu-id="49804-107">EXAMPLES</span></span>

### <span data-ttu-id="49804-108">範例 1-啟用伺服器高級威脅防護</span><span class="sxs-lookup"><span data-stu-id="49804-108">Example 1 - Enable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="49804-109">範例 2-從伺服器資源啟用伺服器高級威脅防護</span><span class="sxs-lookup"><span data-stu-id="49804-109">Example 2 - Enable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="49804-110">參數</span><span class="sxs-lookup"><span data-stu-id="49804-110">PARAMETERS</span></span>

### <span data-ttu-id="49804-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49804-111">-DefaultProfile</span></span>
<span data-ttu-id="49804-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49804-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49804-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49804-113">-InputObject</span></span>
<span data-ttu-id="49804-114">要搭配高級威脅防護原則操作使用的伺服器物件</span><span class="sxs-lookup"><span data-stu-id="49804-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="49804-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49804-115">-ResourceGroupName</span></span>
<span data-ttu-id="49804-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="49804-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="49804-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="49804-117">-ServerName</span></span>
<span data-ttu-id="49804-118">SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="49804-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="49804-119">-確認</span><span class="sxs-lookup"><span data-stu-id="49804-119">-Confirm</span></span>
<span data-ttu-id="49804-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="49804-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49804-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49804-121">-WhatIf</span></span>
<span data-ttu-id="49804-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="49804-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49804-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49804-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49804-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49804-124">CommonParameters</span></span>
<span data-ttu-id="49804-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49804-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49804-126">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="49804-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49804-127">輸入</span><span class="sxs-lookup"><span data-stu-id="49804-127">INPUTS</span></span>

### <span data-ttu-id="49804-128">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="49804-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="49804-129">System.object</span><span class="sxs-lookup"><span data-stu-id="49804-129">System.String</span></span>

## <span data-ttu-id="49804-130">輸出</span><span class="sxs-lookup"><span data-stu-id="49804-130">OUTPUTS</span></span>

### <span data-ttu-id="49804-131">ServerAdvancedThreatProtectionPolicyModel 中的 [AdvancedThreatProtection]</span><span class="sxs-lookup"><span data-stu-id="49804-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="49804-132">筆記</span><span class="sxs-lookup"><span data-stu-id="49804-132">NOTES</span></span>

## <span data-ttu-id="49804-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="49804-133">RELATED LINKS</span></span>
