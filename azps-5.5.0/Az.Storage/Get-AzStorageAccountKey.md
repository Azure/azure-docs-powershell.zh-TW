---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137806"
---
# <span data-ttu-id="f87f3-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f87f3-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="f87f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f87f3-102">SYNOPSIS</span></span>
<span data-ttu-id="f87f3-103">取得 Azure 儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="f87f3-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="f87f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="f87f3-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f87f3-105">說明</span><span class="sxs-lookup"><span data-stu-id="f87f3-105">DESCRIPTION</span></span>
<span data-ttu-id="f87f3-106">**AzStorageAccountKey** Cmdlet 會取得 Azure 儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="f87f3-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="f87f3-107">示例</span><span class="sxs-lookup"><span data-stu-id="f87f3-107">EXAMPLES</span></span>

### <span data-ttu-id="f87f3-108">範例1：取得儲存空間帳戶的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="f87f3-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="f87f3-109">這個命令會取得指定 Azure 儲存空間帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="f87f3-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="f87f3-110">範例2：取得儲存空間帳戶的特定便捷鍵</span><span class="sxs-lookup"><span data-stu-id="f87f3-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### <span data-ttu-id="f87f3-111">範例3：列出儲存空間帳戶的便捷鍵，在 active directory 已啟用的情況下包含 Kerberos 金鑰 () </span><span class="sxs-lookup"><span data-stu-id="f87f3-111">Example 3: Lists the access keys for a Storage account, include the Kerberos keys (if active directory enabled)</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

<span data-ttu-id="f87f3-112">這個命令會取得指定 Azure 儲存空間帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="f87f3-112">This command gets the keys for the specified Azure Storage account.</span></span>

## <span data-ttu-id="f87f3-113">參數</span><span class="sxs-lookup"><span data-stu-id="f87f3-113">PARAMETERS</span></span>

### <span data-ttu-id="f87f3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f87f3-114">-DefaultProfile</span></span>
<span data-ttu-id="f87f3-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f87f3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f87f3-116">-ListKerbKey</span><span class="sxs-lookup"><span data-stu-id="f87f3-116">-ListKerbKey</span></span>
<span data-ttu-id="f87f3-117">如果已為指定的儲存空間帳戶啟用 active directory) ，請列出 Kerberos 金鑰 (。</span><span class="sxs-lookup"><span data-stu-id="f87f3-117">Lists the Kerberos keys (if active directory enabled) for the specified storage account.</span></span>
<span data-ttu-id="f87f3-118">根據 azure Active Directory 網域服務 (azure AD DS) 或 Active Directory 網域服務 (AD DS) ，針對 Azure 檔案身分識別驗證針對每個儲存空間帳戶產生 Kerberos 金鑰。</span><span class="sxs-lookup"><span data-stu-id="f87f3-118">Kerberos key is generated per storage account for Azure Files identity based authentication either with Azure Active Directory Domain Service (Azure AD DS) or Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="f87f3-119">它是用來在代表儲存空間帳戶的網域服務中註冊之身分識別的密碼。</span><span class="sxs-lookup"><span data-stu-id="f87f3-119">It is used as the password of the identity registered in the domain service that represents the storage account.</span></span> <span data-ttu-id="f87f3-120">Kerberos 金鑰不會提供存取權限，以針對儲存空間帳戶執行任何控制或資料平面的讀取或寫入作業。</span><span class="sxs-lookup"><span data-stu-id="f87f3-120">Kerberos key does not provide access permission to perform any control or data plane read or write operations against the storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f87f3-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f87f3-121">-Name</span></span>
<span data-ttu-id="f87f3-122">指定此 Cmdlet 取得金鑰的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f87f3-122">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="f87f3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f87f3-123">-ResourceGroupName</span></span>
<span data-ttu-id="f87f3-124">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f87f3-124">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="f87f3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f87f3-125">CommonParameters</span></span>
<span data-ttu-id="f87f3-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f87f3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f87f3-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f87f3-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f87f3-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f87f3-128">INPUTS</span></span>

### <span data-ttu-id="f87f3-129">System.object</span><span class="sxs-lookup"><span data-stu-id="f87f3-129">System.String</span></span>

## <span data-ttu-id="f87f3-130">輸出</span><span class="sxs-lookup"><span data-stu-id="f87f3-130">OUTPUTS</span></span>

### <span data-ttu-id="f87f3-131">StorageAccountKey （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="f87f3-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="f87f3-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f87f3-132">NOTES</span></span>

## <span data-ttu-id="f87f3-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="f87f3-133">RELATED LINKS</span></span>

[<span data-ttu-id="f87f3-134">新-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f87f3-134">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


