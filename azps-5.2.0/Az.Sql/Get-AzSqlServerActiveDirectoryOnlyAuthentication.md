---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: e5460fcbc48d36dab6309891247315f0539ff7ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280599"
---
# <span data-ttu-id="f9b31-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="f9b31-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="f9b31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9b31-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b31-103">針對特定的 SQL Server，取得 Azure AD 專用驗證。</span><span class="sxs-lookup"><span data-stu-id="f9b31-103">Gets Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="f9b31-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9b31-104">SYNTAX</span></span>

### <span data-ttu-id="f9b31-105">UseResourceGroupAndServerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f9b31-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9b31-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9b31-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9b31-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9b31-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9b31-108">說明</span><span class="sxs-lookup"><span data-stu-id="f9b31-108">DESCRIPTION</span></span>
<span data-ttu-id="f9b31-109">**AzSqlServerActiveDirectoryOnlyAuthentication** Cmdlet 會取得 Azure Active Directory (azure AD) 僅針對目前訂閱中的 AzureSQL 伺服器進行驗證需求。</span><span class="sxs-lookup"><span data-stu-id="f9b31-109">The **Get-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="f9b31-110">示例</span><span class="sxs-lookup"><span data-stu-id="f9b31-110">EXAMPLES</span></span>

### <span data-ttu-id="f9b31-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f9b31-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="f9b31-112">這個命令會取得 Azure Active Directory (Azure AD) 只有與名為 Server01 的資源群組相關聯之 AzureSQL 伺服器的驗證需求。</span><span class="sxs-lookup"><span data-stu-id="f9b31-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="f9b31-113">參數</span><span class="sxs-lookup"><span data-stu-id="f9b31-113">PARAMETERS</span></span>

### <span data-ttu-id="f9b31-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b31-114">-DefaultProfile</span></span>
<span data-ttu-id="f9b31-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9b31-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9b31-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9b31-116">-InputObject</span></span>
<span data-ttu-id="f9b31-117">要使用的 SQL server 物件。</span><span class="sxs-lookup"><span data-stu-id="f9b31-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="f9b31-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9b31-118">-ResourceGroupName</span></span>
<span data-ttu-id="f9b31-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9b31-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="f9b31-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9b31-120">-ResourceId</span></span>
<span data-ttu-id="f9b31-121">要使用之實例的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f9b31-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="f9b31-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f9b31-122">-ServerName</span></span>
<span data-ttu-id="f9b31-123">Azure Active Directory 僅限驗證的 Azure SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="f9b31-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="f9b31-124">-確認</span><span class="sxs-lookup"><span data-stu-id="f9b31-124">-Confirm</span></span>
<span data-ttu-id="f9b31-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f9b31-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9b31-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9b31-126">-WhatIf</span></span>
<span data-ttu-id="f9b31-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9b31-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9b31-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9b31-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9b31-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b31-129">CommonParameters</span></span>
<span data-ttu-id="f9b31-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9b31-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b31-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f9b31-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b31-132">輸入</span><span class="sxs-lookup"><span data-stu-id="f9b31-132">INPUTS</span></span>

### <span data-ttu-id="f9b31-133">System.object</span><span class="sxs-lookup"><span data-stu-id="f9b31-133">System.String</span></span>

## <span data-ttu-id="f9b31-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f9b31-134">OUTPUTS</span></span>

### <span data-ttu-id="f9b31-135">AzureSqlServerActiveDirectoryOnlyAuthenticationModel 中的 [ServerActiveDirectoryAdministrator]</span><span class="sxs-lookup"><span data-stu-id="f9b31-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="f9b31-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f9b31-136">NOTES</span></span>

## <span data-ttu-id="f9b31-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9b31-137">RELATED LINKS</span></span>

[<span data-ttu-id="f9b31-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="f9b31-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="f9b31-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="f9b31-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="f9b31-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f9b31-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="f9b31-141">AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f9b31-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="f9b31-142">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="f9b31-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)