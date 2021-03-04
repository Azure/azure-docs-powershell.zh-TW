---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/enable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: c96b1b9a7eb715f2ab7f02c7e3f86191ac756296
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912310"
---
# <span data-ttu-id="0fa99-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="0fa99-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="0fa99-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0fa99-102">SYNOPSIS</span></span>
<span data-ttu-id="0fa99-103">僅啟用特定 SQL Managed 實例的 Azure AD 驗證。</span><span class="sxs-lookup"><span data-stu-id="0fa99-103">Enables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="0fa99-104">語法</span><span class="sxs-lookup"><span data-stu-id="0fa99-104">SYNTAX</span></span>

### <span data-ttu-id="0fa99-105">UseResourceGroupAndInstanceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0fa99-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fa99-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fa99-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fa99-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fa99-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fa99-108">描述</span><span class="sxs-lookup"><span data-stu-id="0fa99-108">DESCRIPTION</span></span>
<span data-ttu-id="0fa99-109">**Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** Cmdlet 啟用 Azure Active Directory (Azure AD) 目前訂閱中 AzureSQL 受管理實例的驗證需求。</span><span class="sxs-lookup"><span data-stu-id="0fa99-109">The **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="0fa99-110">例子</span><span class="sxs-lookup"><span data-stu-id="0fa99-110">EXAMPLES</span></span>

### <span data-ttu-id="0fa99-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="0fa99-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="0fa99-112">此命令會啟用 Azure Active Directory (Azure AD) 與名為 ResourceGroup01 的資源群組相關聯的 AzureSQL Managed Instance Managed Instance 的驗證需求。</span><span class="sxs-lookup"><span data-stu-id="0fa99-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="0fa99-113">參數</span><span class="sxs-lookup"><span data-stu-id="0fa99-113">PARAMETERS</span></span>

### <span data-ttu-id="0fa99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fa99-114">-DefaultProfile</span></span>
<span data-ttu-id="0fa99-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0fa99-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fa99-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fa99-116">-InputObject</span></span>
<span data-ttu-id="0fa99-117">這是要使用的受管理實例物件。</span><span class="sxs-lookup"><span data-stu-id="0fa99-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="0fa99-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0fa99-118">-InstanceName</span></span>
<span data-ttu-id="0fa99-119">Azure SQL Managed 實例的名稱，只有 Azure Active Directory 驗證才位於其中。</span><span class="sxs-lookup"><span data-stu-id="0fa99-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="0fa99-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fa99-120">-ResourceGroupName</span></span>
<span data-ttu-id="0fa99-121">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0fa99-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="0fa99-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fa99-122">-ResourceId</span></span>
<span data-ttu-id="0fa99-123">要使用實例的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0fa99-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="0fa99-124">-確認</span><span class="sxs-lookup"><span data-stu-id="0fa99-124">-Confirm</span></span>
<span data-ttu-id="0fa99-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0fa99-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fa99-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fa99-126">-WhatIf</span></span>
<span data-ttu-id="0fa99-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0fa99-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fa99-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0fa99-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fa99-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fa99-129">CommonParameters</span></span>
<span data-ttu-id="0fa99-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0fa99-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fa99-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fa99-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fa99-132">輸入</span><span class="sxs-lookup"><span data-stu-id="0fa99-132">INPUTS</span></span>

### <span data-ttu-id="0fa99-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0fa99-133">System.String</span></span>

## <span data-ttu-id="0fa99-134">輸出</span><span class="sxs-lookup"><span data-stu-id="0fa99-134">OUTPUTS</span></span>

### <span data-ttu-id="0fa99-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="0fa99-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="0fa99-136">筆記</span><span class="sxs-lookup"><span data-stu-id="0fa99-136">NOTES</span></span>

## <span data-ttu-id="0fa99-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="0fa99-137">RELATED LINKS</span></span>

[<span data-ttu-id="0fa99-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="0fa99-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="0fa99-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="0fa99-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="0fa99-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="0fa99-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="0fa99-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="0fa99-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)