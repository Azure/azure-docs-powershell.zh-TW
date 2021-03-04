---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: cd540965b4de64b5fbdc5158faedf00f7a3516b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915154"
---
# <span data-ttu-id="f7bcc-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f7bcc-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="f7bcc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f7bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="f7bcc-103">取得 Azure 儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="f7bcc-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="f7bcc-104">語法</span><span class="sxs-lookup"><span data-stu-id="f7bcc-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7bcc-105">描述</span><span class="sxs-lookup"><span data-stu-id="f7bcc-105">DESCRIPTION</span></span>
<span data-ttu-id="f7bcc-106">**Get-AzStorageAccountKey** Cmdlet 會取得 Azure 儲存體帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="f7bcc-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="f7bcc-107">例子</span><span class="sxs-lookup"><span data-stu-id="f7bcc-107">EXAMPLES</span></span>

### <span data-ttu-id="f7bcc-108">範例 1：取得儲存空間帳戶的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="f7bcc-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="f7bcc-109">此命令會獲得指定 Azure 儲存空間帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="f7bcc-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="f7bcc-110">範例 2：取得儲存空間帳戶的特定便捷鍵</span><span class="sxs-lookup"><span data-stu-id="f7bcc-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### <span data-ttu-id="f7bcc-111">範例 3：列出儲存空間帳戶的便捷鍵，包括 Kerberos 鍵 (啟用 Active Directory 時) </span><span class="sxs-lookup"><span data-stu-id="f7bcc-111">Example 3: Lists the access keys for a Storage account, include the Kerberos keys (if active directory enabled)</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

<span data-ttu-id="f7bcc-112">此命令會獲得指定 Azure 儲存空間帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="f7bcc-112">This command gets the keys for the specified Azure Storage account.</span></span>

## <span data-ttu-id="f7bcc-113">參數</span><span class="sxs-lookup"><span data-stu-id="f7bcc-113">PARAMETERS</span></span>

### <span data-ttu-id="f7bcc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7bcc-114">-DefaultProfile</span></span>
<span data-ttu-id="f7bcc-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7bcc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7bcc-116">-ListKerbKey</span><span class="sxs-lookup"><span data-stu-id="f7bcc-116">-ListKerbKey</span></span>
<span data-ttu-id="f7bcc-117">列出指定儲存 (啟用 active directory 時) Kerberos 鍵。</span><span class="sxs-lookup"><span data-stu-id="f7bcc-117">Lists the Kerberos keys (if active directory enabled) for the specified storage account.</span></span>
<span data-ttu-id="f7bcc-118">針對 Azure Active Directory 網域服務 (Azure AD DS) 或 Active Directory 網域服務 (AD DS) ，每個儲存帳戶都產生 Kerberos 金鑰。</span><span class="sxs-lookup"><span data-stu-id="f7bcc-118">Kerberos key is generated per storage account for Azure Files identity based authentication either with Azure Active Directory Domain Service (Azure AD DS) or Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="f7bcc-119">它是用來做為代表儲存帳戶之網域服務所登錄之身分識別的密碼。</span><span class="sxs-lookup"><span data-stu-id="f7bcc-119">It is used as the password of the identity registered in the domain service that represents the storage account.</span></span> <span data-ttu-id="f7bcc-120">Kerberos 金鑰不提供存取權限，無法針對儲存帳戶執行任何控制項或資料面讀取或寫入作業。</span><span class="sxs-lookup"><span data-stu-id="f7bcc-120">Kerberos key does not provide access permission to perform any control or data plane read or write operations against the storage account.</span></span>

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

### <span data-ttu-id="f7bcc-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7bcc-121">-Name</span></span>
<span data-ttu-id="f7bcc-122">指定此 Cmdlet 會獲得金鑰的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f7bcc-122">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="f7bcc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7bcc-123">-ResourceGroupName</span></span>
<span data-ttu-id="f7bcc-124">指定包含儲存空間帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f7bcc-124">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="f7bcc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7bcc-125">CommonParameters</span></span>
<span data-ttu-id="f7bcc-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f7bcc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7bcc-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f7bcc-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7bcc-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f7bcc-128">INPUTS</span></span>

### <span data-ttu-id="f7bcc-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f7bcc-129">System.String</span></span>

## <span data-ttu-id="f7bcc-130">輸出</span><span class="sxs-lookup"><span data-stu-id="f7bcc-130">OUTPUTS</span></span>

### <span data-ttu-id="f7bcc-131">Microsoft.Azure.management.storage.models.StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f7bcc-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="f7bcc-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f7bcc-132">NOTES</span></span>

## <span data-ttu-id="f7bcc-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7bcc-133">RELATED LINKS</span></span>

[<span data-ttu-id="f7bcc-134">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f7bcc-134">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


