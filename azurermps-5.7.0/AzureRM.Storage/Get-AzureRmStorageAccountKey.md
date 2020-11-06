---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: 23066206607289d531f2e2eaa14f90660360a705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445940"
---
# <span data-ttu-id="f93c2-101">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f93c2-101">Get-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="f93c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f93c2-102">SYNOPSIS</span></span>
<span data-ttu-id="f93c2-103">取得 Azure 儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="f93c2-103">Gets the access keys for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f93c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="f93c2-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="f93c2-105">說明</span><span class="sxs-lookup"><span data-stu-id="f93c2-105">DESCRIPTION</span></span>
<span data-ttu-id="f93c2-106">**AzureRmStorageAccountKey** Cmdlet 會取得 Azure 儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="f93c2-106">The **Get-AzureRmStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="f93c2-107">示例</span><span class="sxs-lookup"><span data-stu-id="f93c2-107">EXAMPLES</span></span>

### <span data-ttu-id="f93c2-108">範例1：取得儲存空間帳戶的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="f93c2-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="f93c2-109">這個命令會取得指定 Azure 儲存空間帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="f93c2-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="f93c2-110">範例2：取得儲存空間帳戶的特定便捷鍵</span><span class="sxs-lookup"><span data-stu-id="f93c2-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Key1
```

## <span data-ttu-id="f93c2-111">參數</span><span class="sxs-lookup"><span data-stu-id="f93c2-111">PARAMETERS</span></span>

### <span data-ttu-id="f93c2-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="f93c2-112">-Name</span></span>
<span data-ttu-id="f93c2-113">指定此 Cmdlet 取得金鑰的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f93c2-113">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f93c2-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f93c2-114">-ResourceGroupName</span></span>
<span data-ttu-id="f93c2-115">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f93c2-115">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="f93c2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f93c2-116">CommonParameters</span></span>
<span data-ttu-id="f93c2-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f93c2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f93c2-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f93c2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f93c2-119">輸入</span><span class="sxs-lookup"><span data-stu-id="f93c2-119">INPUTS</span></span>

### <span data-ttu-id="f93c2-120">所有</span><span class="sxs-lookup"><span data-stu-id="f93c2-120">None</span></span>
<span data-ttu-id="f93c2-121">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f93c2-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f93c2-122">輸出</span><span class="sxs-lookup"><span data-stu-id="f93c2-122">OUTPUTS</span></span>

## <span data-ttu-id="f93c2-123">筆記</span><span class="sxs-lookup"><span data-stu-id="f93c2-123">NOTES</span></span>

## <span data-ttu-id="f93c2-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="f93c2-124">RELATED LINKS</span></span>

[<span data-ttu-id="f93c2-125">新-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f93c2-125">New-AzureRmStorageAccountKey</span></span>](./New-AzureRmStorageAccountKey.md)
