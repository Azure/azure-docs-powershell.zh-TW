---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 4b63568b4a2bfd6b79c51fcd906819f4831a7ade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625053"
---
# <span data-ttu-id="47558-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="47558-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="47558-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47558-102">SYNOPSIS</span></span>
<span data-ttu-id="47558-103">取得伺服器長保留期保存庫。</span><span class="sxs-lookup"><span data-stu-id="47558-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47558-104">句法</span><span class="sxs-lookup"><span data-stu-id="47558-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47558-105">說明</span><span class="sxs-lookup"><span data-stu-id="47558-105">DESCRIPTION</span></span>
<span data-ttu-id="47558-106">**AzureRmSqlServerBackupLongTermRetentionVault** Cmdlet 會取得已登錄至此伺服器的長期保留式保險存儲區。</span><span class="sxs-lookup"><span data-stu-id="47558-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="47558-107">Vault 是用來儲存備份資料的 Azure 備份資源。</span><span class="sxs-lookup"><span data-stu-id="47558-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="47558-108">示例</span><span class="sxs-lookup"><span data-stu-id="47558-108">EXAMPLES</span></span>

## <span data-ttu-id="47558-109">參數</span><span class="sxs-lookup"><span data-stu-id="47558-109">PARAMETERS</span></span>

### <span data-ttu-id="47558-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47558-110">-ResourceGroupName</span></span>
<span data-ttu-id="47558-111">指定包含伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="47558-111">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="47558-112">-ServerName</span><span class="sxs-lookup"><span data-stu-id="47558-112">-ServerName</span></span>
<span data-ttu-id="47558-113">指定此 Cmdlet 取得其電子倉庫的伺服器。</span><span class="sxs-lookup"><span data-stu-id="47558-113">Specifies the server for which this cmdlet gets a vault.</span></span>

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

### <span data-ttu-id="47558-114">-確認</span><span class="sxs-lookup"><span data-stu-id="47558-114">-Confirm</span></span>
<span data-ttu-id="47558-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="47558-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47558-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47558-116">-WhatIf</span></span>
<span data-ttu-id="47558-117">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="47558-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47558-118">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47558-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47558-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47558-119">-DefaultProfile</span></span>
<span data-ttu-id="47558-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="47558-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47558-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47558-121">CommonParameters</span></span>
<span data-ttu-id="47558-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47558-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47558-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="47558-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47558-124">輸入</span><span class="sxs-lookup"><span data-stu-id="47558-124">INPUTS</span></span>

## <span data-ttu-id="47558-125">輸出</span><span class="sxs-lookup"><span data-stu-id="47558-125">OUTPUTS</span></span>

## <span data-ttu-id="47558-126">筆記</span><span class="sxs-lookup"><span data-stu-id="47558-126">NOTES</span></span>

## <span data-ttu-id="47558-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="47558-127">RELATED LINKS</span></span>

[<span data-ttu-id="47558-128">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="47558-128">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="47558-129">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="47558-129">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
