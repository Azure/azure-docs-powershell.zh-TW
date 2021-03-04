---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/enable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: edc6ac0a9fd98b2876bc320f392e9038fb76741a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912561"
---
# <span data-ttu-id="83499-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="83499-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="83499-102">簡介</span><span class="sxs-lookup"><span data-stu-id="83499-102">SYNOPSIS</span></span>
<span data-ttu-id="83499-103">僅啟用特定 SQL Server 的 Azure AD 驗證。</span><span class="sxs-lookup"><span data-stu-id="83499-103">Enables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="83499-104">語法</span><span class="sxs-lookup"><span data-stu-id="83499-104">SYNTAX</span></span>

### <span data-ttu-id="83499-105">UseResourceGroupAndServerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="83499-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83499-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83499-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83499-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="83499-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83499-108">描述</span><span class="sxs-lookup"><span data-stu-id="83499-108">DESCRIPTION</span></span>
<span data-ttu-id="83499-109">**Enable-AzSqlServerActiveDirectoryOnlyAuthentication** Cmdlet 啟用 Azure Active Directory (Azure AD) 目前訂閱中 AzureSQL Server 的驗證需求。</span><span class="sxs-lookup"><span data-stu-id="83499-109">The **Enable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="83499-110">例子</span><span class="sxs-lookup"><span data-stu-id="83499-110">EXAMPLES</span></span>

### <span data-ttu-id="83499-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="83499-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="83499-112">此命令會啟用 Azure Active Directory (Azure AD) 與名為 ResourceGroup01 的資源群組相關聯的 AzureSQL 伺服器僅需要驗證。</span><span class="sxs-lookup"><span data-stu-id="83499-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="83499-113">參數</span><span class="sxs-lookup"><span data-stu-id="83499-113">PARAMETERS</span></span>

### <span data-ttu-id="83499-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83499-114">-DefaultProfile</span></span>
<span data-ttu-id="83499-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="83499-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83499-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83499-116">-InputObject</span></span>
<span data-ttu-id="83499-117">這是要使用的 SQL 伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="83499-117">The SQL server object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83499-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83499-118">-ResourceGroupName</span></span>
<span data-ttu-id="83499-119">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="83499-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83499-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83499-120">-ResourceId</span></span>
<span data-ttu-id="83499-121">要使用實例的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="83499-121">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83499-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="83499-122">-ServerName</span></span>
<span data-ttu-id="83499-123">Azure SQL Server 的名稱僅包含 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="83499-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83499-124">-確認</span><span class="sxs-lookup"><span data-stu-id="83499-124">-Confirm</span></span>
<span data-ttu-id="83499-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="83499-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83499-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83499-126">-WhatIf</span></span>
<span data-ttu-id="83499-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="83499-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83499-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="83499-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83499-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83499-129">CommonParameters</span></span>
<span data-ttu-id="83499-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="83499-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83499-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83499-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83499-132">輸入</span><span class="sxs-lookup"><span data-stu-id="83499-132">INPUTS</span></span>

### <span data-ttu-id="83499-133">System.String</span><span class="sxs-lookup"><span data-stu-id="83499-133">System.String</span></span>

## <span data-ttu-id="83499-134">輸出</span><span class="sxs-lookup"><span data-stu-id="83499-134">OUTPUTS</span></span>

### <span data-ttu-id="83499-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="83499-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="83499-136">筆記</span><span class="sxs-lookup"><span data-stu-id="83499-136">NOTES</span></span>

## <span data-ttu-id="83499-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="83499-137">RELATED LINKS</span></span>

[<span data-ttu-id="83499-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="83499-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="83499-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="83499-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="83499-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="83499-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="83499-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="83499-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="83499-142">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="83499-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)