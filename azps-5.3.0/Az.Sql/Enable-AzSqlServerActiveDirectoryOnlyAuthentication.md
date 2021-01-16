---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 002dbbf0a5d244f992beb8a6591907a4c38ed6ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285788"
---
# <span data-ttu-id="7f7dd-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="7f7dd-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="7f7dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f7dd-102">SYNOPSIS</span></span>
<span data-ttu-id="7f7dd-103">針對特定的 SQL Server 啟用 Azure AD 專用驗證。</span><span class="sxs-lookup"><span data-stu-id="7f7dd-103">Enables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="7f7dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f7dd-104">SYNTAX</span></span>

### <span data-ttu-id="7f7dd-105">UseResourceGroupAndServerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7f7dd-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f7dd-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f7dd-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f7dd-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f7dd-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f7dd-108">說明</span><span class="sxs-lookup"><span data-stu-id="7f7dd-108">DESCRIPTION</span></span>
<span data-ttu-id="7f7dd-109">**Enable-AzSqlServerActiveDirectoryOnlyAuthentication** Cmdlet 會啟用 Azure Active Directory (azure AD) 僅針對目前訂閱中的 AzureSQL 伺服器進行驗證需求。</span><span class="sxs-lookup"><span data-stu-id="7f7dd-109">The **Enable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="7f7dd-110">示例</span><span class="sxs-lookup"><span data-stu-id="7f7dd-110">EXAMPLES</span></span>

### <span data-ttu-id="7f7dd-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7f7dd-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="7f7dd-112">這個命令會啟用 Azure Active Directory (Azure AD) 只有一個名為 Server01 的 AzureSQL 伺服器的驗證需求，該伺服器與名為 ResourceGroup01 的資源群組相關聯。</span><span class="sxs-lookup"><span data-stu-id="7f7dd-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="7f7dd-113">參數</span><span class="sxs-lookup"><span data-stu-id="7f7dd-113">PARAMETERS</span></span>

### <span data-ttu-id="7f7dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f7dd-114">-DefaultProfile</span></span>
<span data-ttu-id="7f7dd-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f7dd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f7dd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f7dd-116">-InputObject</span></span>
<span data-ttu-id="7f7dd-117">要使用的 SQL server 物件。</span><span class="sxs-lookup"><span data-stu-id="7f7dd-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="7f7dd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f7dd-118">-ResourceGroupName</span></span>
<span data-ttu-id="7f7dd-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f7dd-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="7f7dd-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f7dd-120">-ResourceId</span></span>
<span data-ttu-id="7f7dd-121">要使用之實例的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7f7dd-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="7f7dd-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7f7dd-122">-ServerName</span></span>
<span data-ttu-id="7f7dd-123">Azure Active Directory 僅限驗證的 Azure SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="7f7dd-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="7f7dd-124">-確認</span><span class="sxs-lookup"><span data-stu-id="7f7dd-124">-Confirm</span></span>
<span data-ttu-id="7f7dd-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7f7dd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f7dd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f7dd-126">-WhatIf</span></span>
<span data-ttu-id="7f7dd-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7f7dd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f7dd-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7f7dd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f7dd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f7dd-129">CommonParameters</span></span>
<span data-ttu-id="7f7dd-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f7dd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f7dd-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7f7dd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f7dd-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7f7dd-132">INPUTS</span></span>

### <span data-ttu-id="7f7dd-133">System.object</span><span class="sxs-lookup"><span data-stu-id="7f7dd-133">System.String</span></span>

## <span data-ttu-id="7f7dd-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7f7dd-134">OUTPUTS</span></span>

### <span data-ttu-id="7f7dd-135">AzureSqlServerActiveDirectoryOnlyAuthenticationModel 中的 [ServerActiveDirectoryAdministrator]</span><span class="sxs-lookup"><span data-stu-id="7f7dd-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="7f7dd-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7f7dd-136">NOTES</span></span>

## <span data-ttu-id="7f7dd-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f7dd-137">RELATED LINKS</span></span>

[<span data-ttu-id="7f7dd-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="7f7dd-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="7f7dd-139">AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="7f7dd-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="7f7dd-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7f7dd-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="7f7dd-141">AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7f7dd-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="7f7dd-142">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="7f7dd-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)