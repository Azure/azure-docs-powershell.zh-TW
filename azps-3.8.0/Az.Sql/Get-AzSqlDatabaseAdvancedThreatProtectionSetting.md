---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 9035f2a03ac04a9bc99248c48675ab3c69b84207
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415184"
---
# <span data-ttu-id="bb66e-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="bb66e-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="bb66e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bb66e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb66e-103">為資料庫獲取進位威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="bb66e-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="bb66e-104">語法</span><span class="sxs-lookup"><span data-stu-id="bb66e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSetting [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb66e-105">描述</span><span class="sxs-lookup"><span data-stu-id="bb66e-105">DESCRIPTION</span></span>
<span data-ttu-id="bb66e-106">**Get-AzSqlDatabaseAdvancedThreatProtectionSetting** Cmdlet 會取得 Azure SQL 資料庫的進級威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="bb66e-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="bb66e-107">若要使用此 Cmdlet，請指定 *ResourceGroupName、ServerName* 和 *DatabaseName* 參數，以識別此 Cmdlet 可進行設定的資料庫。 </span><span class="sxs-lookup"><span data-stu-id="bb66e-107">To use this cmdlet, specify the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="bb66e-108">例子</span><span class="sxs-lookup"><span data-stu-id="bb66e-108">EXAMPLES</span></span>

### <span data-ttu-id="bb66e-109">範例 1：取得資料庫的進一步威脅防護設定</span><span class="sxs-lookup"><span data-stu-id="bb66e-109">Example 1: Get the advanced threat protection settings for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="bb66e-110">此命令會針對名為 Database01 的資料庫，獲得進位威脅防護設定。</span><span class="sxs-lookup"><span data-stu-id="bb66e-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="bb66e-111">資料庫位於伺服器名稱為 Server01，伺服器會指派給資源群組 ResourceGroup11。</span><span class="sxs-lookup"><span data-stu-id="bb66e-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="bb66e-112">參數</span><span class="sxs-lookup"><span data-stu-id="bb66e-112">PARAMETERS</span></span>

### <span data-ttu-id="bb66e-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bb66e-113">-DatabaseName</span></span>
<span data-ttu-id="bb66e-114">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb66e-114">Specifies the name of a database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb66e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb66e-115">-DefaultProfile</span></span>
<span data-ttu-id="bb66e-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="bb66e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb66e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb66e-117">-ResourceGroupName</span></span>
<span data-ttu-id="bb66e-118">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="bb66e-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="bb66e-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bb66e-119">-ServerName</span></span>
<span data-ttu-id="bb66e-120">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb66e-120">Specifies the name of a server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb66e-121">-確認</span><span class="sxs-lookup"><span data-stu-id="bb66e-121">-Confirm</span></span>
<span data-ttu-id="bb66e-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bb66e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb66e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb66e-123">-WhatIf</span></span>
<span data-ttu-id="bb66e-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bb66e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb66e-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb66e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb66e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb66e-126">CommonParameters</span></span>
<span data-ttu-id="bb66e-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bb66e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb66e-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb66e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb66e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="bb66e-129">INPUTS</span></span>

### <span data-ttu-id="bb66e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bb66e-130">System.String</span></span>

## <span data-ttu-id="bb66e-131">輸出</span><span class="sxs-lookup"><span data-stu-id="bb66e-131">OUTPUTS</span></span>

### <span data-ttu-id="bb66e-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="bb66e-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="bb66e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="bb66e-133">NOTES</span></span>

## <span data-ttu-id="bb66e-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb66e-134">RELATED LINKS</span></span>




