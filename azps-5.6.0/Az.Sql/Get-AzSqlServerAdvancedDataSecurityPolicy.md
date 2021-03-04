---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 372951b708d34c44706f981424b7ace39efff2b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907469"
---
# <span data-ttu-id="9bfd2-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="9bfd2-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="9bfd2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9bfd2-102">SYNOPSIS</span></span>
<span data-ttu-id="9bfd2-103">獲得伺服器的進位資料安全性原則。</span><span class="sxs-lookup"><span data-stu-id="9bfd2-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="9bfd2-104">語法</span><span class="sxs-lookup"><span data-stu-id="9bfd2-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bfd2-105">描述</span><span class="sxs-lookup"><span data-stu-id="9bfd2-105">DESCRIPTION</span></span>
<span data-ttu-id="9bfd2-106">**Get-AzSqlServerAdvancedDataSecurityPolicy** Cmdlet 會取得伺服器的進一步資料安全性原則。</span><span class="sxs-lookup"><span data-stu-id="9bfd2-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="9bfd2-107">例子</span><span class="sxs-lookup"><span data-stu-id="9bfd2-107">EXAMPLES</span></span>

### <span data-ttu-id="9bfd2-108">範例 1：獲取伺服器進位資料安全性</span><span class="sxs-lookup"><span data-stu-id="9bfd2-108">Example 1: Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="9bfd2-109">範例 2：從伺服器資源獲取伺服器進位資料安全性</span><span class="sxs-lookup"><span data-stu-id="9bfd2-109">Example 2: Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="9bfd2-110">參數</span><span class="sxs-lookup"><span data-stu-id="9bfd2-110">PARAMETERS</span></span>

### <span data-ttu-id="9bfd2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bfd2-111">-DefaultProfile</span></span>
<span data-ttu-id="9bfd2-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9bfd2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bfd2-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bfd2-113">-InputObject</span></span>
<span data-ttu-id="9bfd2-114">要與進一階段資料安全性原則作業一起使用的伺服器物件</span><span class="sxs-lookup"><span data-stu-id="9bfd2-114">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bfd2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bfd2-115">-ResourceGroupName</span></span>
<span data-ttu-id="9bfd2-116">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9bfd2-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="9bfd2-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9bfd2-117">-ServerName</span></span>
<span data-ttu-id="9bfd2-118">SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="9bfd2-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="9bfd2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bfd2-119">CommonParameters</span></span>
<span data-ttu-id="9bfd2-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9bfd2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bfd2-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9bfd2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bfd2-122">輸入</span><span class="sxs-lookup"><span data-stu-id="9bfd2-122">INPUTS</span></span>

### <span data-ttu-id="9bfd2-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="9bfd2-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="9bfd2-124">System.String</span><span class="sxs-lookup"><span data-stu-id="9bfd2-124">System.String</span></span>

## <span data-ttu-id="9bfd2-125">輸出</span><span class="sxs-lookup"><span data-stu-id="9bfd2-125">OUTPUTS</span></span>

### <span data-ttu-id="9bfd2-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="9bfd2-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="9bfd2-127">筆記</span><span class="sxs-lookup"><span data-stu-id="9bfd2-127">NOTES</span></span>

## <span data-ttu-id="9bfd2-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="9bfd2-128">RELATED LINKS</span></span>
