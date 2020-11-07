---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: faecfdf62892faba2f7ec1241d7e02daa1e6ed12
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958242"
---
# <span data-ttu-id="c5a70-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c5a70-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="c5a70-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c5a70-102">SYNOPSIS</span></span>
<span data-ttu-id="c5a70-103">取得 Azure 儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="c5a70-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="c5a70-104">句法</span><span class="sxs-lookup"><span data-stu-id="c5a70-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5a70-105">說明</span><span class="sxs-lookup"><span data-stu-id="c5a70-105">DESCRIPTION</span></span>
<span data-ttu-id="c5a70-106">**AzStorageAccountKey** Cmdlet 會取得 Azure 儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="c5a70-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="c5a70-107">示例</span><span class="sxs-lookup"><span data-stu-id="c5a70-107">EXAMPLES</span></span>

### <span data-ttu-id="c5a70-108">範例1：取得儲存空間帳戶的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="c5a70-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="c5a70-109">這個命令會取得指定 Azure 儲存空間帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="c5a70-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="c5a70-110">範例2：取得儲存空間帳戶的特定便捷鍵</span><span class="sxs-lookup"><span data-stu-id="c5a70-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

## <span data-ttu-id="c5a70-111">參數</span><span class="sxs-lookup"><span data-stu-id="c5a70-111">PARAMETERS</span></span>

### <span data-ttu-id="c5a70-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5a70-112">-DefaultProfile</span></span>
<span data-ttu-id="c5a70-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5a70-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5a70-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="c5a70-114">-Name</span></span>
<span data-ttu-id="c5a70-115">指定此 Cmdlet 取得金鑰的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c5a70-115">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="c5a70-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5a70-116">-ResourceGroupName</span></span>
<span data-ttu-id="c5a70-117">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5a70-117">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="c5a70-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5a70-118">CommonParameters</span></span>
<span data-ttu-id="c5a70-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c5a70-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5a70-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c5a70-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5a70-121">輸入</span><span class="sxs-lookup"><span data-stu-id="c5a70-121">INPUTS</span></span>

### <span data-ttu-id="c5a70-122">System.object</span><span class="sxs-lookup"><span data-stu-id="c5a70-122">System.String</span></span>

## <span data-ttu-id="c5a70-123">輸出</span><span class="sxs-lookup"><span data-stu-id="c5a70-123">OUTPUTS</span></span>

### <span data-ttu-id="c5a70-124">StorageAccountKey （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="c5a70-124">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="c5a70-125">筆記</span><span class="sxs-lookup"><span data-stu-id="c5a70-125">NOTES</span></span>

## <span data-ttu-id="c5a70-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5a70-126">RELATED LINKS</span></span>

[<span data-ttu-id="c5a70-127">新-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c5a70-127">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


