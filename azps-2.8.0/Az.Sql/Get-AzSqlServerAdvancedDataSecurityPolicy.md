---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 74956ff74beeb166a7788d0e577a86a4d2538ded
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792487"
---
# <span data-ttu-id="a355e-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="a355e-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="a355e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a355e-102">SYNOPSIS</span></span>
<span data-ttu-id="a355e-103">取得伺服器的高級資料安全性原則。</span><span class="sxs-lookup"><span data-stu-id="a355e-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="a355e-104">句法</span><span class="sxs-lookup"><span data-stu-id="a355e-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a355e-105">說明</span><span class="sxs-lookup"><span data-stu-id="a355e-105">DESCRIPTION</span></span>
<span data-ttu-id="a355e-106">**AzSqlServerAdvancedDataSecurityPolicy** Cmdlet 會檢索伺服器的 [高級資料] 安全原則。</span><span class="sxs-lookup"><span data-stu-id="a355e-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="a355e-107">示例</span><span class="sxs-lookup"><span data-stu-id="a355e-107">EXAMPLES</span></span>

### <span data-ttu-id="a355e-108">範例 1-取得伺服器高級資料安全性</span><span class="sxs-lookup"><span data-stu-id="a355e-108">Example 1 - Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="a355e-109">範例 2-從伺服器資源取得伺服器高級資料安全性</span><span class="sxs-lookup"><span data-stu-id="a355e-109">Example 2 - Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="a355e-110">參數</span><span class="sxs-lookup"><span data-stu-id="a355e-110">PARAMETERS</span></span>

### <span data-ttu-id="a355e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a355e-111">-DefaultProfile</span></span>
<span data-ttu-id="a355e-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a355e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a355e-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a355e-113">-InputObject</span></span>
<span data-ttu-id="a355e-114">要搭配高級資料安全性原則作業使用的伺服器物件</span><span class="sxs-lookup"><span data-stu-id="a355e-114">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a355e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a355e-115">-ResourceGroupName</span></span>
<span data-ttu-id="a355e-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a355e-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="a355e-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a355e-117">-ServerName</span></span>
<span data-ttu-id="a355e-118">SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="a355e-118">SQL Database server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a355e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a355e-119">CommonParameters</span></span>
<span data-ttu-id="a355e-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a355e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a355e-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a355e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a355e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a355e-122">INPUTS</span></span>

### <span data-ttu-id="a355e-123">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="a355e-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="a355e-124">System.object</span><span class="sxs-lookup"><span data-stu-id="a355e-124">System.String</span></span>

## <span data-ttu-id="a355e-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a355e-125">OUTPUTS</span></span>

### <span data-ttu-id="a355e-126">ServerAdvancedDataSecurityPolicyModel 中的 [AdvancedThreatProtection]</span><span class="sxs-lookup"><span data-stu-id="a355e-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="a355e-127">筆記</span><span class="sxs-lookup"><span data-stu-id="a355e-127">NOTES</span></span>

## <span data-ttu-id="a355e-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="a355e-128">RELATED LINKS</span></span>