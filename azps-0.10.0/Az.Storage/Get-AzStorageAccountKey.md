---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: e44ad10adf9e07a1e8096469be4c82c88b1dbe0c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795162"
---
# <span data-ttu-id="bcdc0-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bcdc0-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="bcdc0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bcdc0-102">SYNOPSIS</span></span>
<span data-ttu-id="bcdc0-103">取得 Azure 儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="bcdc0-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="bcdc0-104">句法</span><span class="sxs-lookup"><span data-stu-id="bcdc0-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcdc0-105">說明</span><span class="sxs-lookup"><span data-stu-id="bcdc0-105">DESCRIPTION</span></span>
<span data-ttu-id="bcdc0-106">**AzStorageAccountKey** Cmdlet 會取得 Azure 儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="bcdc0-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="bcdc0-107">示例</span><span class="sxs-lookup"><span data-stu-id="bcdc0-107">EXAMPLES</span></span>

### <span data-ttu-id="bcdc0-108">範例1：取得儲存空間帳戶的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="bcdc0-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="bcdc0-109">這個命令會取得指定 Azure 儲存空間帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="bcdc0-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="bcdc0-110">範例2：取得儲存空間帳戶的特定便捷鍵</span><span class="sxs-lookup"><span data-stu-id="bcdc0-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

## <span data-ttu-id="bcdc0-111">參數</span><span class="sxs-lookup"><span data-stu-id="bcdc0-111">PARAMETERS</span></span>

### <span data-ttu-id="bcdc0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcdc0-112">-DefaultProfile</span></span>
<span data-ttu-id="bcdc0-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bcdc0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcdc0-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="bcdc0-114">-Name</span></span>
<span data-ttu-id="bcdc0-115">指定此 Cmdlet 取得金鑰的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="bcdc0-115">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="bcdc0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcdc0-116">-ResourceGroupName</span></span>
<span data-ttu-id="bcdc0-117">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcdc0-117">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="bcdc0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcdc0-118">CommonParameters</span></span>
<span data-ttu-id="bcdc0-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bcdc0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcdc0-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bcdc0-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcdc0-121">輸入</span><span class="sxs-lookup"><span data-stu-id="bcdc0-121">INPUTS</span></span>

### <span data-ttu-id="bcdc0-122">System.object</span><span class="sxs-lookup"><span data-stu-id="bcdc0-122">System.String</span></span>

## <span data-ttu-id="bcdc0-123">輸出</span><span class="sxs-lookup"><span data-stu-id="bcdc0-123">OUTPUTS</span></span>

### <span data-ttu-id="bcdc0-124">StorageAccountKey （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="bcdc0-124">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="bcdc0-125">筆記</span><span class="sxs-lookup"><span data-stu-id="bcdc0-125">NOTES</span></span>

## <span data-ttu-id="bcdc0-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcdc0-126">RELATED LINKS</span></span>

[<span data-ttu-id="bcdc0-127">新-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bcdc0-127">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


