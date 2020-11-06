---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
ms.openlocfilehash: a168b48089052ed8daa764407254d04084ece771
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446824"
---
# <span data-ttu-id="45075-101">Enable-AzureRmDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="45075-101">Enable-AzureRmDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="45075-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45075-102">SYNOPSIS</span></span>
<span data-ttu-id="45075-103">嘗試啟用使用者管理的金鑰保存庫以加密指定的資料 Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="45075-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45075-104">句法</span><span class="sxs-lookup"><span data-stu-id="45075-104">SYNTAX</span></span>

```
Enable-AzureRmDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45075-105">說明</span><span class="sxs-lookup"><span data-stu-id="45075-105">DESCRIPTION</span></span>
<span data-ttu-id="45075-106">**Enable-AzureRmDataLakeStoreKeyVault** Cmdlet 會嘗試啟用使用者管理的金鑰保存庫，以加密指定的資料 Lake store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="45075-106">The **Enable-AzureRmDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="45075-107">示例</span><span class="sxs-lookup"><span data-stu-id="45075-107">EXAMPLES</span></span>

### <span data-ttu-id="45075-108">範例1：為 ContosoADLS 帳戶啟用金鑰保存庫</span><span class="sxs-lookup"><span data-stu-id="45075-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzureRmDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="45075-109">這個命令會嘗試針對名為 ContosoADLS 的 Data Lake Store 帳戶啟用使用者管理的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="45075-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="45075-110">參數</span><span class="sxs-lookup"><span data-stu-id="45075-110">PARAMETERS</span></span>

### <span data-ttu-id="45075-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="45075-111">-Account</span></span>
<span data-ttu-id="45075-112">要啟用使用者管理的金鑰保存庫的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="45075-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45075-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45075-113">-ResourceGroupName</span></span>
<span data-ttu-id="45075-114">與帳戶相關聯之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="45075-114">Name of resource group associated with the account.</span></span> <span data-ttu-id="45075-115">如果未指定，將會嘗試探索。</span><span class="sxs-lookup"><span data-stu-id="45075-115">If not specified will attempt to be discovered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45075-116">-確認</span><span class="sxs-lookup"><span data-stu-id="45075-116">-Confirm</span></span>
<span data-ttu-id="45075-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="45075-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45075-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45075-118">-WhatIf</span></span>
<span data-ttu-id="45075-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="45075-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45075-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45075-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45075-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45075-121">-DefaultProfile</span></span>
<span data-ttu-id="45075-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45075-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45075-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45075-123">CommonParameters</span></span>
<span data-ttu-id="45075-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45075-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45075-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45075-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45075-126">輸入</span><span class="sxs-lookup"><span data-stu-id="45075-126">INPUTS</span></span>

### <span data-ttu-id="45075-127">System.object</span><span class="sxs-lookup"><span data-stu-id="45075-127">System.String</span></span>

## <span data-ttu-id="45075-128">輸出</span><span class="sxs-lookup"><span data-stu-id="45075-128">OUTPUTS</span></span>

## <span data-ttu-id="45075-129">筆記</span><span class="sxs-lookup"><span data-stu-id="45075-129">NOTES</span></span>

## <span data-ttu-id="45075-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="45075-130">RELATED LINKS</span></span>

[<span data-ttu-id="45075-131">新-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="45075-131">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="45075-132">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="45075-132">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

