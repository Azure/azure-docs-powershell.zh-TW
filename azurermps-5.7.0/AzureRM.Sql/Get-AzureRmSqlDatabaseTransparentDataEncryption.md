---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 5136da99879e4636018ae1a01cc95f39f2924b4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450463"
---
# <span data-ttu-id="0f22c-101">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="0f22c-101">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="0f22c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0f22c-102">SYNOPSIS</span></span>
<span data-ttu-id="0f22c-103">取得資料庫的 TDE 狀態。</span><span class="sxs-lookup"><span data-stu-id="0f22c-103">Gets the TDE state for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f22c-104">句法</span><span class="sxs-lookup"><span data-stu-id="0f22c-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f22c-105">說明</span><span class="sxs-lookup"><span data-stu-id="0f22c-105">DESCRIPTION</span></span>
<span data-ttu-id="0f22c-106">**AzureRmSqlDatabaseTransparentDataEncryption** Cmdlet 會取得 Azure SQL Database 的透明資料加密的狀態 (TDE) 。</span><span class="sxs-lookup"><span data-stu-id="0f22c-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="0f22c-107">如需詳細資訊，請參閱 https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) Microsoft 開發人員網路文件庫中與 Azure SQL Database (的透明資料加密。</span><span class="sxs-lookup"><span data-stu-id="0f22c-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="0f22c-108">這個 Cmdlet 會取得 TDE 的目前狀態，但加密和解密可能是長時間執行的作業。</span><span class="sxs-lookup"><span data-stu-id="0f22c-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="0f22c-109">若要查看加密掃描進度，請執行 Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f22c-109">To see the encryption scan progress, run the Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>

<span data-ttu-id="0f22c-110">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f22c-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0f22c-111">示例</span><span class="sxs-lookup"><span data-stu-id="0f22c-111">EXAMPLES</span></span>

### <span data-ttu-id="0f22c-112">範例1：取得資料庫的 TDE 狀態</span><span class="sxs-lookup"><span data-stu-id="0f22c-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="0f22c-113">這個命令會取得名為 server01 之伺服器上名為 Database01 之資料庫的 TDE 狀態。</span><span class="sxs-lookup"><span data-stu-id="0f22c-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="0f22c-114">參數</span><span class="sxs-lookup"><span data-stu-id="0f22c-114">PARAMETERS</span></span>

### <span data-ttu-id="0f22c-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0f22c-115">-DatabaseName</span></span>
<span data-ttu-id="0f22c-116">指定此 Cmdlet 取得 TDE 狀態之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f22c-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f22c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f22c-117">-DefaultProfile</span></span>
<span data-ttu-id="0f22c-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0f22c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f22c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f22c-119">-ResourceGroupName</span></span>
<span data-ttu-id="0f22c-120">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f22c-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="0f22c-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0f22c-121">-ServerName</span></span>
<span data-ttu-id="0f22c-122">指定承載此 Cmdlet 之 TDE 狀態之資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="0f22c-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f22c-123">-確認</span><span class="sxs-lookup"><span data-stu-id="0f22c-123">-Confirm</span></span>
<span data-ttu-id="0f22c-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0f22c-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f22c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f22c-125">-WhatIf</span></span>
<span data-ttu-id="0f22c-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0f22c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f22c-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f22c-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f22c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f22c-128">CommonParameters</span></span>
<span data-ttu-id="0f22c-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0f22c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f22c-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0f22c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f22c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="0f22c-131">INPUTS</span></span>

### <span data-ttu-id="0f22c-132">所有</span><span class="sxs-lookup"><span data-stu-id="0f22c-132">None</span></span>
<span data-ttu-id="0f22c-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="0f22c-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0f22c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="0f22c-134">OUTPUTS</span></span>

### <span data-ttu-id="0f22c-135">AzureSqlDatabaseTransparentDataEncryptionModel 中的 [TransparentDataEncryption]</span><span class="sxs-lookup"><span data-stu-id="0f22c-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="0f22c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="0f22c-136">NOTES</span></span>

## <span data-ttu-id="0f22c-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f22c-137">RELATED LINKS</span></span>

[<span data-ttu-id="0f22c-138">AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="0f22c-138">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="0f22c-139">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="0f22c-139">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)