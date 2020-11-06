---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: 16762b56995b90422c78ad6dc5dd87461c0a8317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451011"
---
# <span data-ttu-id="1ec41-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1ec41-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="1ec41-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ec41-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec41-103">取得伺服器的高級威脅防護原則。</span><span class="sxs-lookup"><span data-stu-id="1ec41-103">Gets Advanced Threat Protection policy of a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ec41-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ec41-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ec41-105">說明</span><span class="sxs-lookup"><span data-stu-id="1ec41-105">DESCRIPTION</span></span>
<span data-ttu-id="1ec41-106">**AzureRmSqlServerAdvancedThreatProtectionPolicy** Cmdlet retrives 伺服器的高級威脅防護原則。</span><span class="sxs-lookup"><span data-stu-id="1ec41-106">The **Get-AzureRmSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="1ec41-107">示例</span><span class="sxs-lookup"><span data-stu-id="1ec41-107">EXAMPLES</span></span>

### <span data-ttu-id="1ec41-108">範例 1-取得伺服器高級威脅防護</span><span class="sxs-lookup"><span data-stu-id="1ec41-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="1ec41-109">範例 2-從伺服器資源取得伺服器高級威脅防護</span><span class="sxs-lookup"><span data-stu-id="1ec41-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzureRmSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="1ec41-110">參數</span><span class="sxs-lookup"><span data-stu-id="1ec41-110">PARAMETERS</span></span>

### <span data-ttu-id="1ec41-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec41-111">-DefaultProfile</span></span>
<span data-ttu-id="1ec41-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ec41-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ec41-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ec41-113">-InputObject</span></span>
<span data-ttu-id="1ec41-114">要搭配高級威脅防護原則操作使用的伺服器物件</span><span class="sxs-lookup"><span data-stu-id="1ec41-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="1ec41-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ec41-115">-ResourceGroupName</span></span>
<span data-ttu-id="1ec41-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ec41-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="1ec41-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1ec41-117">-ServerName</span></span>
<span data-ttu-id="1ec41-118">SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1ec41-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="1ec41-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec41-119">CommonParameters</span></span>
<span data-ttu-id="1ec41-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ec41-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec41-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1ec41-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec41-122">輸入</span><span class="sxs-lookup"><span data-stu-id="1ec41-122">INPUTS</span></span>

### <span data-ttu-id="1ec41-123">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="1ec41-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="1ec41-124">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="1ec41-124">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="1ec41-125">System.object</span><span class="sxs-lookup"><span data-stu-id="1ec41-125">System.String</span></span>

## <span data-ttu-id="1ec41-126">輸出</span><span class="sxs-lookup"><span data-stu-id="1ec41-126">OUTPUTS</span></span>

### <span data-ttu-id="1ec41-127">ServerAdvancedThreatProtectionPolicyModel 中的 [AdvancedThreatProtection]</span><span class="sxs-lookup"><span data-stu-id="1ec41-127">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="1ec41-128">筆記</span><span class="sxs-lookup"><span data-stu-id="1ec41-128">NOTES</span></span>

## <span data-ttu-id="1ec41-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ec41-129">RELATED LINKS</span></span>
