---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 2d9fa7ef7d3763d2db1d963aa1b1cac41b711bd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917550"
---
# <span data-ttu-id="f41d1-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="f41d1-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="f41d1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f41d1-102">SYNOPSIS</span></span>
<span data-ttu-id="f41d1-103">獲得受管理實例的進位資料安全性原則。</span><span class="sxs-lookup"><span data-stu-id="f41d1-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="f41d1-104">語法</span><span class="sxs-lookup"><span data-stu-id="f41d1-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f41d1-105">描述</span><span class="sxs-lookup"><span data-stu-id="f41d1-105">DESCRIPTION</span></span>
<span data-ttu-id="f41d1-106">**Get-AzSqlInstanceAdvancedDataSecurityPolicy** Cmdlet 會從受管理實例中取得進位資料安全性原則。</span><span class="sxs-lookup"><span data-stu-id="f41d1-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="f41d1-107">例子</span><span class="sxs-lookup"><span data-stu-id="f41d1-107">EXAMPLES</span></span>

### <span data-ttu-id="f41d1-108">範例 1：獲得受管理實例進位資料安全性</span><span class="sxs-lookup"><span data-stu-id="f41d1-108">Example 1: Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="f41d1-109">範例 2：從受管理實例資源獲得受管理實例進一步資料安全性</span><span class="sxs-lookup"><span data-stu-id="f41d1-109">Example 2: Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="f41d1-110">參數</span><span class="sxs-lookup"><span data-stu-id="f41d1-110">PARAMETERS</span></span>

### <span data-ttu-id="f41d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f41d1-111">-DefaultProfile</span></span>
<span data-ttu-id="f41d1-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f41d1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f41d1-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f41d1-113">-InputObject</span></span>
<span data-ttu-id="f41d1-114">要與進一階段資料安全性原則作業一起使用的受管理實例物件</span><span class="sxs-lookup"><span data-stu-id="f41d1-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="f41d1-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f41d1-115">-InstanceName</span></span>
<span data-ttu-id="f41d1-116">SQL Database 受管理的實例名稱。</span><span class="sxs-lookup"><span data-stu-id="f41d1-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="f41d1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f41d1-117">-ResourceGroupName</span></span>
<span data-ttu-id="f41d1-118">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f41d1-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="f41d1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f41d1-119">CommonParameters</span></span>
<span data-ttu-id="f41d1-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f41d1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f41d1-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f41d1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f41d1-122">輸入</span><span class="sxs-lookup"><span data-stu-id="f41d1-122">INPUTS</span></span>

### <span data-ttu-id="f41d1-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="f41d1-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="f41d1-124">System.String</span><span class="sxs-lookup"><span data-stu-id="f41d1-124">System.String</span></span>

## <span data-ttu-id="f41d1-125">輸出</span><span class="sxs-lookup"><span data-stu-id="f41d1-125">OUTPUTS</span></span>

### <span data-ttu-id="f41d1-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f41d1-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="f41d1-127">筆記</span><span class="sxs-lookup"><span data-stu-id="f41d1-127">NOTES</span></span>

## <span data-ttu-id="f41d1-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="f41d1-128">RELATED LINKS</span></span>
