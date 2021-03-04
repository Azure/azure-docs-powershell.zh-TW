---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 4abe17fb272e97637bbd43a69401f9c101f14ef6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905818"
---
# <span data-ttu-id="89cb1-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="89cb1-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="89cb1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="89cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="89cb1-103">停用伺服器上進位的資料安全性。</span><span class="sxs-lookup"><span data-stu-id="89cb1-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="89cb1-104">語法</span><span class="sxs-lookup"><span data-stu-id="89cb1-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89cb1-105">描述</span><span class="sxs-lookup"><span data-stu-id="89cb1-105">DESCRIPTION</span></span>
<span data-ttu-id="89cb1-106">**Disable-AzSqlServerAdvancedDataSecurity** Cmdlet 會停用伺服器上進位的資料安全性。</span><span class="sxs-lookup"><span data-stu-id="89cb1-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="89cb1-107">例子</span><span class="sxs-lookup"><span data-stu-id="89cb1-107">EXAMPLES</span></span>

### <span data-ttu-id="89cb1-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="89cb1-108">Example 1</span></span>
### <span data-ttu-id="89cb1-109">範例 2：停用伺服器進位資料安全性</span><span class="sxs-lookup"><span data-stu-id="89cb1-109">Example 2: Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="89cb1-110">範例 3：從伺服器資源停用伺服器進位資料安全性</span><span class="sxs-lookup"><span data-stu-id="89cb1-110">Example 3: Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="89cb1-111">參數</span><span class="sxs-lookup"><span data-stu-id="89cb1-111">PARAMETERS</span></span>

### <span data-ttu-id="89cb1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89cb1-112">-DefaultProfile</span></span>
<span data-ttu-id="89cb1-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="89cb1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89cb1-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89cb1-114">-InputObject</span></span>
<span data-ttu-id="89cb1-115">要與進一階段資料安全性原則作業一起使用的伺服器物件</span><span class="sxs-lookup"><span data-stu-id="89cb1-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="89cb1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89cb1-116">-ResourceGroupName</span></span>
<span data-ttu-id="89cb1-117">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="89cb1-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="89cb1-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="89cb1-118">-ServerName</span></span>
<span data-ttu-id="89cb1-119">SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="89cb1-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="89cb1-120">-確認</span><span class="sxs-lookup"><span data-stu-id="89cb1-120">-Confirm</span></span>
<span data-ttu-id="89cb1-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="89cb1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89cb1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89cb1-122">-WhatIf</span></span>
<span data-ttu-id="89cb1-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="89cb1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89cb1-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="89cb1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89cb1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89cb1-125">CommonParameters</span></span>
<span data-ttu-id="89cb1-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="89cb1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89cb1-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89cb1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89cb1-128">輸入</span><span class="sxs-lookup"><span data-stu-id="89cb1-128">INPUTS</span></span>

### <span data-ttu-id="89cb1-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="89cb1-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="89cb1-130">System.String</span><span class="sxs-lookup"><span data-stu-id="89cb1-130">System.String</span></span>

## <span data-ttu-id="89cb1-131">輸出</span><span class="sxs-lookup"><span data-stu-id="89cb1-131">OUTPUTS</span></span>

### <span data-ttu-id="89cb1-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="89cb1-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="89cb1-133">筆記</span><span class="sxs-lookup"><span data-stu-id="89cb1-133">NOTES</span></span>

## <span data-ttu-id="89cb1-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="89cb1-134">RELATED LINKS</span></span>
