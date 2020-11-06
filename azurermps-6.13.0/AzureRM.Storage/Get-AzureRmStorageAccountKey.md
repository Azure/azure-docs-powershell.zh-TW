---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: 08d997caef7280d922a01dbea127bd4db64cd28f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443695"
---
# <span data-ttu-id="a333b-101">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a333b-101">Get-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="a333b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a333b-102">SYNOPSIS</span></span>
<span data-ttu-id="a333b-103">取得 Azure 儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="a333b-103">Gets the access keys for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a333b-104">句法</span><span class="sxs-lookup"><span data-stu-id="a333b-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a333b-105">說明</span><span class="sxs-lookup"><span data-stu-id="a333b-105">DESCRIPTION</span></span>
<span data-ttu-id="a333b-106">**AzureRmStorageAccountKey** Cmdlet 會取得 Azure 儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="a333b-106">The **Get-AzureRmStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="a333b-107">示例</span><span class="sxs-lookup"><span data-stu-id="a333b-107">EXAMPLES</span></span>

### <span data-ttu-id="a333b-108">範例1：取得儲存空間帳戶的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="a333b-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="a333b-109">這個命令會取得指定 Azure 儲存空間帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="a333b-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="a333b-110">範例2：取得儲存空間帳戶的特定便捷鍵</span><span class="sxs-lookup"><span data-stu-id="a333b-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

## <span data-ttu-id="a333b-111">參數</span><span class="sxs-lookup"><span data-stu-id="a333b-111">PARAMETERS</span></span>

### <span data-ttu-id="a333b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a333b-112">-DefaultProfile</span></span>
<span data-ttu-id="a333b-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a333b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a333b-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="a333b-114">-Name</span></span>
<span data-ttu-id="a333b-115">指定此 Cmdlet 取得金鑰的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a333b-115">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a333b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a333b-116">-ResourceGroupName</span></span>
<span data-ttu-id="a333b-117">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a333b-117">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="a333b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a333b-118">CommonParameters</span></span>
<span data-ttu-id="a333b-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a333b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a333b-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a333b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a333b-121">輸入</span><span class="sxs-lookup"><span data-stu-id="a333b-121">INPUTS</span></span>

### <span data-ttu-id="a333b-122">System.object</span><span class="sxs-lookup"><span data-stu-id="a333b-122">System.String</span></span>

## <span data-ttu-id="a333b-123">輸出</span><span class="sxs-lookup"><span data-stu-id="a333b-123">OUTPUTS</span></span>

### <span data-ttu-id="a333b-124">StorageAccountKey （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="a333b-124">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="a333b-125">筆記</span><span class="sxs-lookup"><span data-stu-id="a333b-125">NOTES</span></span>

## <span data-ttu-id="a333b-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="a333b-126">RELATED LINKS</span></span>

[<span data-ttu-id="a333b-127">新-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a333b-127">New-AzureRmStorageAccountKey</span></span>](./New-AzureRmStorageAccountKey.md)


