---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 10788eea0c3571450a483888945ab591d7ddf13b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142971"
---
# <span data-ttu-id="41866-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="41866-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="41866-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41866-102">SYNOPSIS</span></span>
<span data-ttu-id="41866-103">針對特定的 SQL Managed 實例取得 Azure AD 僅限驗證。</span><span class="sxs-lookup"><span data-stu-id="41866-103">Gets Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="41866-104">句法</span><span class="sxs-lookup"><span data-stu-id="41866-104">SYNTAX</span></span>

### <span data-ttu-id="41866-105">UseResourceGroupAndInstanceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="41866-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41866-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41866-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41866-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41866-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41866-108">說明</span><span class="sxs-lookup"><span data-stu-id="41866-108">DESCRIPTION</span></span>
<span data-ttu-id="41866-109">**AzSqlInstanceActiveDirectoryOnlyAuthentication** Cmdlet 會取得 Azure Active Directory (azure AD) 只有目前訂閱中 AzureSQL 受管理實例的驗證需求。</span><span class="sxs-lookup"><span data-stu-id="41866-109">The **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="41866-110">示例</span><span class="sxs-lookup"><span data-stu-id="41866-110">EXAMPLES</span></span>

### <span data-ttu-id="41866-111">範例1</span><span class="sxs-lookup"><span data-stu-id="41866-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
```

<span data-ttu-id="41866-112">這個命令會取得 Azure Active Directory (Azure AD) 只有與名為「ResourceGroup01」資源群組相關聯之 AzureSQL Managed 實例的驗證需求。</span><span class="sxs-lookup"><span data-stu-id="41866-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="41866-113">參數</span><span class="sxs-lookup"><span data-stu-id="41866-113">PARAMETERS</span></span>

### <span data-ttu-id="41866-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41866-114">-DefaultProfile</span></span>
<span data-ttu-id="41866-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41866-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41866-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41866-116">-InputObject</span></span>
<span data-ttu-id="41866-117">要使用的 managed 實例物件。</span><span class="sxs-lookup"><span data-stu-id="41866-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="41866-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="41866-118">-InstanceName</span></span>
<span data-ttu-id="41866-119">Azure Active Directory 僅驗證的 Azure SQL Managed 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="41866-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="41866-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41866-120">-ResourceGroupName</span></span>
<span data-ttu-id="41866-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="41866-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="41866-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41866-122">-ResourceId</span></span>
<span data-ttu-id="41866-123">要使用之實例的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="41866-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="41866-124">-確認</span><span class="sxs-lookup"><span data-stu-id="41866-124">-Confirm</span></span>
<span data-ttu-id="41866-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="41866-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41866-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41866-126">-WhatIf</span></span>
<span data-ttu-id="41866-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41866-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41866-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41866-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41866-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41866-129">CommonParameters</span></span>
<span data-ttu-id="41866-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41866-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41866-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="41866-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41866-132">輸入</span><span class="sxs-lookup"><span data-stu-id="41866-132">INPUTS</span></span>

### <span data-ttu-id="41866-133">System.object</span><span class="sxs-lookup"><span data-stu-id="41866-133">System.String</span></span>

## <span data-ttu-id="41866-134">輸出</span><span class="sxs-lookup"><span data-stu-id="41866-134">OUTPUTS</span></span>

### <span data-ttu-id="41866-135">AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel 中的 [InstanceActiveDirectoryOnlyAuthentication]</span><span class="sxs-lookup"><span data-stu-id="41866-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="41866-136">筆記</span><span class="sxs-lookup"><span data-stu-id="41866-136">NOTES</span></span>

## <span data-ttu-id="41866-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="41866-137">RELATED LINKS</span></span>

[<span data-ttu-id="41866-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="41866-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="41866-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="41866-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="41866-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="41866-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="41866-141">AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="41866-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

