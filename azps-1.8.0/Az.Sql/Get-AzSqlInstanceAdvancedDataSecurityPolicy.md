---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 3f67d8197fd56cbcb615e8d95ef4331910ff9080
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620423"
---
# <span data-ttu-id="c8adc-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="c8adc-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="c8adc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8adc-102">SYNOPSIS</span></span>
<span data-ttu-id="c8adc-103">取得受管理實例的高級資料安全性原則。</span><span class="sxs-lookup"><span data-stu-id="c8adc-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="c8adc-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8adc-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8adc-105">說明</span><span class="sxs-lookup"><span data-stu-id="c8adc-105">DESCRIPTION</span></span>
<span data-ttu-id="c8adc-106">**AzSqlInstanceAdvancedDataSecurityPolicy** Cmdlet retrives 受管理實例的「高級資料」安全性原則。</span><span class="sxs-lookup"><span data-stu-id="c8adc-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrives the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="c8adc-107">示例</span><span class="sxs-lookup"><span data-stu-id="c8adc-107">EXAMPLES</span></span>

### <span data-ttu-id="c8adc-108">範例 1-取得受管理的實例高級資料安全性</span><span class="sxs-lookup"><span data-stu-id="c8adc-108">Example 1 - Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="c8adc-109">範例 2-從受管理的實例資源取得 managed 實例高級資料安全性</span><span class="sxs-lookup"><span data-stu-id="c8adc-109">Example 2 - Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="c8adc-110">參數</span><span class="sxs-lookup"><span data-stu-id="c8adc-110">PARAMETERS</span></span>

### <span data-ttu-id="c8adc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8adc-111">-DefaultProfile</span></span>
<span data-ttu-id="c8adc-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8adc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8adc-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8adc-113">-InputObject</span></span>
<span data-ttu-id="c8adc-114">要與高級資料安全性原則作業搭配使用的 managed 實例物件</span><span class="sxs-lookup"><span data-stu-id="c8adc-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="c8adc-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c8adc-115">-InstanceName</span></span>
<span data-ttu-id="c8adc-116">SQL 資料庫管理實例名稱。</span><span class="sxs-lookup"><span data-stu-id="c8adc-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="c8adc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8adc-117">-ResourceGroupName</span></span>
<span data-ttu-id="c8adc-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8adc-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="c8adc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8adc-119">CommonParameters</span></span>
<span data-ttu-id="c8adc-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8adc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8adc-121">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c8adc-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8adc-122">輸入</span><span class="sxs-lookup"><span data-stu-id="c8adc-122">INPUTS</span></span>

### <span data-ttu-id="c8adc-123">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="c8adc-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="c8adc-124">System.object</span><span class="sxs-lookup"><span data-stu-id="c8adc-124">System.String</span></span>

## <span data-ttu-id="c8adc-125">輸出</span><span class="sxs-lookup"><span data-stu-id="c8adc-125">OUTPUTS</span></span>

### <span data-ttu-id="c8adc-126">ManagedInstanceAdvancedDataSecurityPolicyModel 中的 [AdvancedThreatProtection]</span><span class="sxs-lookup"><span data-stu-id="c8adc-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="c8adc-127">筆記</span><span class="sxs-lookup"><span data-stu-id="c8adc-127">NOTES</span></span>

## <span data-ttu-id="c8adc-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8adc-128">RELATED LINKS</span></span>
