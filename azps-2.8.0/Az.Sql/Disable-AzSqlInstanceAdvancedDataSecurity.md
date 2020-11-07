---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: a5aa9029e9d787311bb5b0c13b761c14f2b8bbca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792034"
---
# <span data-ttu-id="0501e-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="0501e-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="0501e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0501e-102">SYNOPSIS</span></span>
<span data-ttu-id="0501e-103">在受管理的實例上停用 [高級資料安全性]。</span><span class="sxs-lookup"><span data-stu-id="0501e-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="0501e-104">句法</span><span class="sxs-lookup"><span data-stu-id="0501e-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0501e-105">說明</span><span class="sxs-lookup"><span data-stu-id="0501e-105">DESCRIPTION</span></span>
<span data-ttu-id="0501e-106">**Disable AzSqlInstanceAdvancedDataSecurity** Cmdlet 會在受管理的實例上停用高級資料安全性。</span><span class="sxs-lookup"><span data-stu-id="0501e-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="0501e-107">示例</span><span class="sxs-lookup"><span data-stu-id="0501e-107">EXAMPLES</span></span>

### <span data-ttu-id="0501e-108">範例 1-停用受管理的實例高級資料安全性</span><span class="sxs-lookup"><span data-stu-id="0501e-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="0501e-109">範例 2-從 managed 實例資源停用伺服器高級資料安全性</span><span class="sxs-lookup"><span data-stu-id="0501e-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="0501e-110">參數</span><span class="sxs-lookup"><span data-stu-id="0501e-110">PARAMETERS</span></span>

### <span data-ttu-id="0501e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0501e-111">-DefaultProfile</span></span>
<span data-ttu-id="0501e-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0501e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0501e-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0501e-113">-InputObject</span></span>
<span data-ttu-id="0501e-114">要與高級資料安全性原則作業搭配使用的 managed 實例物件</span><span class="sxs-lookup"><span data-stu-id="0501e-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="0501e-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0501e-115">-InstanceName</span></span>
<span data-ttu-id="0501e-116">SQL 資料庫管理實例名稱。</span><span class="sxs-lookup"><span data-stu-id="0501e-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="0501e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0501e-117">-ResourceGroupName</span></span>
<span data-ttu-id="0501e-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0501e-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="0501e-119">-確認</span><span class="sxs-lookup"><span data-stu-id="0501e-119">-Confirm</span></span>
<span data-ttu-id="0501e-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0501e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0501e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0501e-121">-WhatIf</span></span>
<span data-ttu-id="0501e-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0501e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0501e-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0501e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0501e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0501e-124">CommonParameters</span></span>
<span data-ttu-id="0501e-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0501e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0501e-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0501e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0501e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="0501e-127">INPUTS</span></span>

### <span data-ttu-id="0501e-128">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="0501e-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="0501e-129">System.object</span><span class="sxs-lookup"><span data-stu-id="0501e-129">System.String</span></span>

## <span data-ttu-id="0501e-130">輸出</span><span class="sxs-lookup"><span data-stu-id="0501e-130">OUTPUTS</span></span>

### <span data-ttu-id="0501e-131">ManagedInstanceAdvancedDataSecurityPolicyModel 中的 [AdvancedThreatProtection]</span><span class="sxs-lookup"><span data-stu-id="0501e-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="0501e-132">筆記</span><span class="sxs-lookup"><span data-stu-id="0501e-132">NOTES</span></span>

## <span data-ttu-id="0501e-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="0501e-133">RELATED LINKS</span></span>
