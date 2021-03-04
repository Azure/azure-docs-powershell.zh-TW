---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 0a06eae51b074cefb74b2ef3a175a056cc52ff84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917558"
---
# <span data-ttu-id="7d533-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="7d533-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="7d533-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7d533-102">SYNOPSIS</span></span>
<span data-ttu-id="7d533-103">僅特定 SQL Managed 實例的 Azure AD 驗證。</span><span class="sxs-lookup"><span data-stu-id="7d533-103">Gets Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="7d533-104">語法</span><span class="sxs-lookup"><span data-stu-id="7d533-104">SYNTAX</span></span>

### <span data-ttu-id="7d533-105">UseResourceGroupAndInstanceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7d533-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d533-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d533-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d533-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d533-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d533-108">描述</span><span class="sxs-lookup"><span data-stu-id="7d533-108">DESCRIPTION</span></span>
<span data-ttu-id="7d533-109">**Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** Cmdlet 會取得 Azure Active Directory (Azure AD) 目前訂閱中 AzureSQL 受管理實例的驗證需求。</span><span class="sxs-lookup"><span data-stu-id="7d533-109">The **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="7d533-110">例子</span><span class="sxs-lookup"><span data-stu-id="7d533-110">EXAMPLES</span></span>

### <span data-ttu-id="7d533-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="7d533-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
```

<span data-ttu-id="7d533-112">此命令會獲得 Azure Active Directory (Azure AD) 與 ResourceGroup01 資源群組相關聯的 AzureSQL Managed Instance Managed Instance 的驗證需求。</span><span class="sxs-lookup"><span data-stu-id="7d533-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="7d533-113">參數</span><span class="sxs-lookup"><span data-stu-id="7d533-113">PARAMETERS</span></span>

### <span data-ttu-id="7d533-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d533-114">-DefaultProfile</span></span>
<span data-ttu-id="7d533-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d533-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d533-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d533-116">-InputObject</span></span>
<span data-ttu-id="7d533-117">這是要使用的受管理實例物件。</span><span class="sxs-lookup"><span data-stu-id="7d533-117">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d533-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7d533-118">-InstanceName</span></span>
<span data-ttu-id="7d533-119">Azure SQL Managed 實例的名稱，只有 Azure Active Directory 驗證才位於其中。</span><span class="sxs-lookup"><span data-stu-id="7d533-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d533-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d533-120">-ResourceGroupName</span></span>
<span data-ttu-id="7d533-121">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d533-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d533-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d533-122">-ResourceId</span></span>
<span data-ttu-id="7d533-123">要使用實例的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7d533-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="7d533-124">-確認</span><span class="sxs-lookup"><span data-stu-id="7d533-124">-Confirm</span></span>
<span data-ttu-id="7d533-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7d533-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d533-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d533-126">-WhatIf</span></span>
<span data-ttu-id="7d533-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7d533-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d533-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d533-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d533-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d533-129">CommonParameters</span></span>
<span data-ttu-id="7d533-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7d533-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d533-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d533-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d533-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7d533-132">INPUTS</span></span>

### <span data-ttu-id="7d533-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7d533-133">System.String</span></span>

## <span data-ttu-id="7d533-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7d533-134">OUTPUTS</span></span>

### <span data-ttu-id="7d533-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="7d533-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="7d533-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7d533-136">NOTES</span></span>

## <span data-ttu-id="7d533-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d533-137">RELATED LINKS</span></span>

[<span data-ttu-id="7d533-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="7d533-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="7d533-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="7d533-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="7d533-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7d533-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="7d533-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7d533-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

