---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: dce8018e97e01c10356e77d321d564690cc03f71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620402"
---
# <span data-ttu-id="c7c7f-101">Get-AzSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c7c7f-101">Get-AzSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="c7c7f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c7f-103">取得伺服器的高級威脅防護原則。</span><span class="sxs-lookup"><span data-stu-id="c7c7f-103">Gets Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="c7c7f-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7c7f-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7c7f-105">說明</span><span class="sxs-lookup"><span data-stu-id="c7c7f-105">DESCRIPTION</span></span>
<span data-ttu-id="c7c7f-106">**AzSqlServerAdvancedThreatProtectionPolicy** Cmdlet retrives 伺服器的高級威脅防護原則。</span><span class="sxs-lookup"><span data-stu-id="c7c7f-106">The **Get-AzSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="c7c7f-107">示例</span><span class="sxs-lookup"><span data-stu-id="c7c7f-107">EXAMPLES</span></span>

### <span data-ttu-id="c7c7f-108">範例 1-取得伺服器高級威脅防護</span><span class="sxs-lookup"><span data-stu-id="c7c7f-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="c7c7f-109">範例 2-從伺服器資源取得伺服器高級威脅防護</span><span class="sxs-lookup"><span data-stu-id="c7c7f-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="c7c7f-110">參數</span><span class="sxs-lookup"><span data-stu-id="c7c7f-110">PARAMETERS</span></span>

### <span data-ttu-id="c7c7f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7c7f-111">-DefaultProfile</span></span>
<span data-ttu-id="c7c7f-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7c7f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7c7f-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7c7f-113">-InputObject</span></span>
<span data-ttu-id="c7c7f-114">要搭配高級威脅防護原則操作使用的伺服器物件</span><span class="sxs-lookup"><span data-stu-id="c7c7f-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="c7c7f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7c7f-115">-ResourceGroupName</span></span>
<span data-ttu-id="c7c7f-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7c7f-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="c7c7f-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c7c7f-117">-ServerName</span></span>
<span data-ttu-id="c7c7f-118">SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="c7c7f-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="c7c7f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c7f-119">CommonParameters</span></span>
<span data-ttu-id="c7c7f-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7c7f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c7f-121">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c7c7f-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c7f-122">輸入</span><span class="sxs-lookup"><span data-stu-id="c7c7f-122">INPUTS</span></span>

### <span data-ttu-id="c7c7f-123">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="c7c7f-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="c7c7f-124">System.object</span><span class="sxs-lookup"><span data-stu-id="c7c7f-124">System.String</span></span>

## <span data-ttu-id="c7c7f-125">輸出</span><span class="sxs-lookup"><span data-stu-id="c7c7f-125">OUTPUTS</span></span>

### <span data-ttu-id="c7c7f-126">ServerAdvancedThreatProtectionPolicyModel 中的 [AdvancedThreatProtection]</span><span class="sxs-lookup"><span data-stu-id="c7c7f-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="c7c7f-127">筆記</span><span class="sxs-lookup"><span data-stu-id="c7c7f-127">NOTES</span></span>

## <span data-ttu-id="c7c7f-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7c7f-128">RELATED LINKS</span></span>
