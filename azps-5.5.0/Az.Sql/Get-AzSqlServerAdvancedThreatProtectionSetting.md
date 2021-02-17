---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: a9d2d82ae9b35b79701d071fa7598cf40b185cd5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413195"
---
# <span data-ttu-id="c4d3a-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="c4d3a-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="c4d3a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c4d3a-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d3a-103">為伺服器獲取進位威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="c4d3a-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="c4d3a-104">語法</span><span class="sxs-lookup"><span data-stu-id="c4d3a-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSetting -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4d3a-105">描述</span><span class="sxs-lookup"><span data-stu-id="c4d3a-105">DESCRIPTION</span></span>
<span data-ttu-id="c4d3a-106">**Get-AzSqlServerAdvancedThreatProtectionSetting** Cmdlet 會取得 Azure SQL 伺服器進一步的威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="c4d3a-106">The **Get-AzSqlServerAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="c4d3a-107">若要使用此 Cmdlet，請指定 *ResourceGroupName* 和 *ServerName* 參數，以識別此 Cmdlet 會獲得設定的伺服器。</span><span class="sxs-lookup"><span data-stu-id="c4d3a-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="c4d3a-108">例子</span><span class="sxs-lookup"><span data-stu-id="c4d3a-108">EXAMPLES</span></span>

### <span data-ttu-id="c4d3a-109">範例 1：取得伺服器的進一步威脅防護設定</span><span class="sxs-lookup"><span data-stu-id="c4d3a-109">Example 1: Get the advanced threat protection settings for a server</span></span>
```
PS C:\>Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="c4d3a-110">此命令會針對伺服器名稱為 Server01 的進一階段威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="c4d3a-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="c4d3a-111">伺服器會指派給資源群組 ResourceGroup11。</span><span class="sxs-lookup"><span data-stu-id="c4d3a-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="c4d3a-112">參數</span><span class="sxs-lookup"><span data-stu-id="c4d3a-112">PARAMETERS</span></span>

### <span data-ttu-id="c4d3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4d3a-113">-DefaultProfile</span></span>
<span data-ttu-id="c4d3a-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c4d3a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4d3a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4d3a-115">-ResourceGroupName</span></span>
<span data-ttu-id="c4d3a-116">指定伺服器所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="c4d3a-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="c4d3a-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c4d3a-117">-ServerName</span></span>
<span data-ttu-id="c4d3a-118">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4d3a-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="c4d3a-119">-確認</span><span class="sxs-lookup"><span data-stu-id="c4d3a-119">-Confirm</span></span>
<span data-ttu-id="c4d3a-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c4d3a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d3a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4d3a-121">-WhatIf</span></span>
<span data-ttu-id="c4d3a-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c4d3a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4d3a-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c4d3a-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d3a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d3a-124">CommonParameters</span></span>
<span data-ttu-id="c4d3a-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c4d3a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d3a-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4d3a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d3a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="c4d3a-127">INPUTS</span></span>

### <span data-ttu-id="c4d3a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c4d3a-128">System.String</span></span>

## <span data-ttu-id="c4d3a-129">輸出</span><span class="sxs-lookup"><span data-stu-id="c4d3a-129">OUTPUTS</span></span>

### <span data-ttu-id="c4d3a-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="c4d3a-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="c4d3a-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c4d3a-131">NOTES</span></span>

## <span data-ttu-id="c4d3a-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4d3a-132">RELATED LINKS</span></span>


[<span data-ttu-id="c4d3a-133">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="c4d3a-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


