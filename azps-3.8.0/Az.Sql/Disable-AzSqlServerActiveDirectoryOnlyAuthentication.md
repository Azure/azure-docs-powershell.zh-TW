---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: a736ede2c84b3fbe782928d7cff14a558b69bcdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957959"
---
# <span data-ttu-id="c56b5-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="c56b5-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="c56b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c56b5-102">SYNOPSIS</span></span>
<span data-ttu-id="c56b5-103">針對特定的 SQL Server 停用 Azure AD 專用驗證。</span><span class="sxs-lookup"><span data-stu-id="c56b5-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="c56b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="c56b5-104">SYNTAX</span></span>

```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c56b5-105">說明</span><span class="sxs-lookup"><span data-stu-id="c56b5-105">DESCRIPTION</span></span>
<span data-ttu-id="c56b5-106">**Disable AzSqlServerActiveDirectoryOnlyAuthentication** Cmdlet 會停用 Azure Active Directory (azure AD) 只有目前訂閱中 AzureSQL 伺服器的驗證需求。</span><span class="sxs-lookup"><span data-stu-id="c56b5-106">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="c56b5-107">示例</span><span class="sxs-lookup"><span data-stu-id="c56b5-107">EXAMPLES</span></span>

### <span data-ttu-id="c56b5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c56b5-108">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="c56b5-109">這個命令會停用 Azure Active Directory (Azure AD) 只有與名為「ResourceGroup01」資源群組相關聯之 AzureSQL 伺服器的驗證需求。</span><span class="sxs-lookup"><span data-stu-id="c56b5-109">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="c56b5-110">參數</span><span class="sxs-lookup"><span data-stu-id="c56b5-110">PARAMETERS</span></span>

### <span data-ttu-id="c56b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c56b5-111">-DefaultProfile</span></span>
<span data-ttu-id="c56b5-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c56b5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c56b5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c56b5-113">-ResourceGroupName</span></span>
<span data-ttu-id="c56b5-114">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c56b5-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="c56b5-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c56b5-115">-ServerName</span></span>
<span data-ttu-id="c56b5-116">Azure Active Directory 系統管理員所在的 Azure SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="c56b5-116">The name of the Azure SQL Server the Azure Active Directory administrator is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c56b5-117">-確認</span><span class="sxs-lookup"><span data-stu-id="c56b5-117">-Confirm</span></span>
<span data-ttu-id="c56b5-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c56b5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c56b5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c56b5-119">-WhatIf</span></span>
<span data-ttu-id="c56b5-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c56b5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c56b5-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c56b5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c56b5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c56b5-122">CommonParameters</span></span>
<span data-ttu-id="c56b5-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c56b5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c56b5-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c56b5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c56b5-125">輸入</span><span class="sxs-lookup"><span data-stu-id="c56b5-125">INPUTS</span></span>

### <span data-ttu-id="c56b5-126">System.object</span><span class="sxs-lookup"><span data-stu-id="c56b5-126">System.String</span></span>

## <span data-ttu-id="c56b5-127">輸出</span><span class="sxs-lookup"><span data-stu-id="c56b5-127">OUTPUTS</span></span>

### <span data-ttu-id="c56b5-128">AzureSqlServerActiveDirectoryAdministratorModel 中的 [ServerActiveDirectoryAdministrator]</span><span class="sxs-lookup"><span data-stu-id="c56b5-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="c56b5-129">筆記</span><span class="sxs-lookup"><span data-stu-id="c56b5-129">NOTES</span></span>

## <span data-ttu-id="c56b5-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="c56b5-130">RELATED LINKS</span></span>

[<span data-ttu-id="c56b5-131">移除-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c56b5-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="c56b5-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c56b5-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="c56b5-133">AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c56b5-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="c56b5-134">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="c56b5-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
