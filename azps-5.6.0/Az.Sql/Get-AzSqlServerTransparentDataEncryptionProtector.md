---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: cd211537949fe3743298ad4cba93ca6c63b7c39b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915222"
---
# <span data-ttu-id="ca1df-101">Get-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ca1df-101">Get-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="ca1df-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ca1df-102">SYNOPSIS</span></span>
<span data-ttu-id="ca1df-103">獲得透明資料加密 (TDE) 程式</span><span class="sxs-lookup"><span data-stu-id="ca1df-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

## <span data-ttu-id="ca1df-104">語法</span><span class="sxs-lookup"><span data-stu-id="ca1df-104">SYNTAX</span></span>

```
Get-AzSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca1df-105">描述</span><span class="sxs-lookup"><span data-stu-id="ca1df-105">DESCRIPTION</span></span>
<span data-ttu-id="ca1df-106">Cmdlet Get-AzSqlServerTransparentDataEncryptionProtector TDE 功能區的資訊。</span><span class="sxs-lookup"><span data-stu-id="ca1df-106">The Get-AzSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="ca1df-107">例子</span><span class="sxs-lookup"><span data-stu-id="ca1df-107">EXAMPLES</span></span>

### <span data-ttu-id="ca1df-108">範例 1：取得透明資料加密 (TDE) 設置</span><span class="sxs-lookup"><span data-stu-id="ca1df-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="ca1df-109">此命令會為名為 ContosoResourceGroup 的資源群組中名為 ContosoServer 的伺服器，獲得 TDE 用戶端。</span><span class="sxs-lookup"><span data-stu-id="ca1df-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="ca1df-110">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="ca1df-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="ca1df-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="ca1df-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="ca1df-112">參數</span><span class="sxs-lookup"><span data-stu-id="ca1df-112">PARAMETERS</span></span>

### <span data-ttu-id="ca1df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca1df-113">-DefaultProfile</span></span>
<span data-ttu-id="ca1df-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ca1df-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca1df-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca1df-115">-ResourceGroupName</span></span>
<span data-ttu-id="ca1df-116">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="ca1df-116">The name of the resource group</span></span>

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

### <span data-ttu-id="ca1df-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ca1df-117">-ServerName</span></span>
<span data-ttu-id="ca1df-118">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="ca1df-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="ca1df-119">-確認</span><span class="sxs-lookup"><span data-stu-id="ca1df-119">-Confirm</span></span>
<span data-ttu-id="ca1df-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ca1df-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca1df-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca1df-121">-WhatIf</span></span>
<span data-ttu-id="ca1df-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca1df-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca1df-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca1df-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca1df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca1df-124">CommonParameters</span></span>
<span data-ttu-id="ca1df-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ca1df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca1df-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca1df-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca1df-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ca1df-127">INPUTS</span></span>

### <span data-ttu-id="ca1df-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ca1df-128">System.String</span></span>

## <span data-ttu-id="ca1df-129">輸出</span><span class="sxs-lookup"><span data-stu-id="ca1df-129">OUTPUTS</span></span>

### <span data-ttu-id="ca1df-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="ca1df-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="ca1df-131">筆記</span><span class="sxs-lookup"><span data-stu-id="ca1df-131">NOTES</span></span>

## <span data-ttu-id="ca1df-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca1df-132">RELATED LINKS</span></span>

[<span data-ttu-id="ca1df-133">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="ca1df-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
