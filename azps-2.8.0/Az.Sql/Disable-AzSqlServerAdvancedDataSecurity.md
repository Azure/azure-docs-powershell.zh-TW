---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: ca3b39ac369900f19c41b27b50efb06af7cf2056
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792378"
---
# <span data-ttu-id="cda56-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="cda56-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="cda56-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cda56-102">SYNOPSIS</span></span>
<span data-ttu-id="cda56-103">在伺服器上停用 [高級資料安全性]。</span><span class="sxs-lookup"><span data-stu-id="cda56-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="cda56-104">句法</span><span class="sxs-lookup"><span data-stu-id="cda56-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cda56-105">說明</span><span class="sxs-lookup"><span data-stu-id="cda56-105">DESCRIPTION</span></span>
<span data-ttu-id="cda56-106">**Disable AzSqlServerAdvancedDataSecurity** Cmdlet 會在伺服器上停用高級資料安全性。</span><span class="sxs-lookup"><span data-stu-id="cda56-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="cda56-107">示例</span><span class="sxs-lookup"><span data-stu-id="cda56-107">EXAMPLES</span></span>

### <span data-ttu-id="cda56-108">範例1</span><span class="sxs-lookup"><span data-stu-id="cda56-108">Example 1</span></span>
### <span data-ttu-id="cda56-109">範例 1-停用伺服器高級資料安全性</span><span class="sxs-lookup"><span data-stu-id="cda56-109">Example 1 - Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="cda56-110">範例 2-從伺服器資源停用伺服器高級資料安全性</span><span class="sxs-lookup"><span data-stu-id="cda56-110">Example 2 - Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="cda56-111">參數</span><span class="sxs-lookup"><span data-stu-id="cda56-111">PARAMETERS</span></span>

### <span data-ttu-id="cda56-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda56-112">-DefaultProfile</span></span>
<span data-ttu-id="cda56-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cda56-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda56-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cda56-114">-InputObject</span></span>
<span data-ttu-id="cda56-115">要搭配高級資料安全性原則作業使用的伺服器物件</span><span class="sxs-lookup"><span data-stu-id="cda56-115">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cda56-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cda56-116">-ResourceGroupName</span></span>
<span data-ttu-id="cda56-117">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cda56-117">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda56-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cda56-118">-ServerName</span></span>
<span data-ttu-id="cda56-119">SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="cda56-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="cda56-120">-確認</span><span class="sxs-lookup"><span data-stu-id="cda56-120">-Confirm</span></span>
<span data-ttu-id="cda56-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cda56-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cda56-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cda56-122">-WhatIf</span></span>
<span data-ttu-id="cda56-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cda56-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cda56-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cda56-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cda56-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda56-125">CommonParameters</span></span>
<span data-ttu-id="cda56-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cda56-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cda56-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cda56-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda56-128">輸入</span><span class="sxs-lookup"><span data-stu-id="cda56-128">INPUTS</span></span>

### <span data-ttu-id="cda56-129">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="cda56-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="cda56-130">System.object</span><span class="sxs-lookup"><span data-stu-id="cda56-130">System.String</span></span>

## <span data-ttu-id="cda56-131">輸出</span><span class="sxs-lookup"><span data-stu-id="cda56-131">OUTPUTS</span></span>

### <span data-ttu-id="cda56-132">ServerAdvancedDataSecurityPolicyModel 中的 [AdvancedThreatProtection]</span><span class="sxs-lookup"><span data-stu-id="cda56-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="cda56-133">筆記</span><span class="sxs-lookup"><span data-stu-id="cda56-133">NOTES</span></span>

## <span data-ttu-id="cda56-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="cda56-134">RELATED LINKS</span></span>
