---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 4116ddf22bb39ddfa78e07180aaf61da7e87bb7f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909458"
---
# <span data-ttu-id="93ca9-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="93ca9-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="93ca9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="93ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="93ca9-103">停用受管理實例上的進位資料安全性。</span><span class="sxs-lookup"><span data-stu-id="93ca9-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="93ca9-104">語法</span><span class="sxs-lookup"><span data-stu-id="93ca9-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93ca9-105">描述</span><span class="sxs-lookup"><span data-stu-id="93ca9-105">DESCRIPTION</span></span>
<span data-ttu-id="93ca9-106">**Disable-AzSqlInstanceAdvancedDataSecurity** Cmdlet 會停用受管理實例上的進位資料安全性。</span><span class="sxs-lookup"><span data-stu-id="93ca9-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="93ca9-107">例子</span><span class="sxs-lookup"><span data-stu-id="93ca9-107">EXAMPLES</span></span>

### <span data-ttu-id="93ca9-108">範例 1 - 停用受管理實例進位資料安全性</span><span class="sxs-lookup"><span data-stu-id="93ca9-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="93ca9-109">範例 2 - 從受管理的實例資源停用伺服器進位資料安全性</span><span class="sxs-lookup"><span data-stu-id="93ca9-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="93ca9-110">參數</span><span class="sxs-lookup"><span data-stu-id="93ca9-110">PARAMETERS</span></span>

### <span data-ttu-id="93ca9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ca9-111">-DefaultProfile</span></span>
<span data-ttu-id="93ca9-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="93ca9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93ca9-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93ca9-113">-InputObject</span></span>
<span data-ttu-id="93ca9-114">要與進一階段資料安全性原則作業一起使用的受管理實例物件</span><span class="sxs-lookup"><span data-stu-id="93ca9-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93ca9-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="93ca9-115">-InstanceName</span></span>
<span data-ttu-id="93ca9-116">SQL Database 受管理的實例名稱。</span><span class="sxs-lookup"><span data-stu-id="93ca9-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="93ca9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93ca9-117">-ResourceGroupName</span></span>
<span data-ttu-id="93ca9-118">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="93ca9-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="93ca9-119">-確認</span><span class="sxs-lookup"><span data-stu-id="93ca9-119">-Confirm</span></span>
<span data-ttu-id="93ca9-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="93ca9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93ca9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93ca9-121">-WhatIf</span></span>
<span data-ttu-id="93ca9-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="93ca9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93ca9-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93ca9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93ca9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ca9-124">CommonParameters</span></span>
<span data-ttu-id="93ca9-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="93ca9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ca9-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93ca9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ca9-127">輸入</span><span class="sxs-lookup"><span data-stu-id="93ca9-127">INPUTS</span></span>

### <span data-ttu-id="93ca9-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="93ca9-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="93ca9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="93ca9-129">System.String</span></span>

## <span data-ttu-id="93ca9-130">輸出</span><span class="sxs-lookup"><span data-stu-id="93ca9-130">OUTPUTS</span></span>

### <span data-ttu-id="93ca9-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="93ca9-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="93ca9-132">筆記</span><span class="sxs-lookup"><span data-stu-id="93ca9-132">NOTES</span></span>

## <span data-ttu-id="93ca9-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="93ca9-133">RELATED LINKS</span></span>
