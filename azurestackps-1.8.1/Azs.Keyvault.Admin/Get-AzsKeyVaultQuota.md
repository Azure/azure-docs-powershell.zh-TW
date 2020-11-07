---
external help file: Azs.KeyVault.Admin-help.xml
Module Name: Azs.Keyvault.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 435db6fd34e36e6c65b9086b7ac1935f60d86c06
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793979"
---
# <span data-ttu-id="ba2cb-101">Get-AzsKeyVaultQuota</span><span class="sxs-lookup"><span data-stu-id="ba2cb-101">Get-AzsKeyVaultQuota</span></span>

## <span data-ttu-id="ba2cb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba2cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ba2cb-103">取得位置上 KeyVault 的所有配額物件的清單。</span><span class="sxs-lookup"><span data-stu-id="ba2cb-103">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="ba2cb-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba2cb-104">SYNTAX</span></span>

```
Get-AzsKeyVaultQuota [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="ba2cb-105">說明</span><span class="sxs-lookup"><span data-stu-id="ba2cb-105">DESCRIPTION</span></span>
<span data-ttu-id="ba2cb-106">取得位置上 KeyVault 的所有配額物件的清單。</span><span class="sxs-lookup"><span data-stu-id="ba2cb-106">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="ba2cb-107">示例</span><span class="sxs-lookup"><span data-stu-id="ba2cb-107">EXAMPLES</span></span>

### <span data-ttu-id="ba2cb-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ba2cb-108">EXAMPLE 1</span></span>
```
Get-AzsKeyVaultQuota
```

<span data-ttu-id="ba2cb-109">取得位置上 KeyVault 的所有配額物件的清單。</span><span class="sxs-lookup"><span data-stu-id="ba2cb-109">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="ba2cb-110">參數</span><span class="sxs-lookup"><span data-stu-id="ba2cb-110">PARAMETERS</span></span>

### <span data-ttu-id="ba2cb-111">-位置</span><span class="sxs-lookup"><span data-stu-id="ba2cb-111">-Location</span></span>
<span data-ttu-id="ba2cb-112">配額的位置。</span><span class="sxs-lookup"><span data-stu-id="ba2cb-112">The location of the quota.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba2cb-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba2cb-113">CommonParameters</span></span>
<span data-ttu-id="ba2cb-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba2cb-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba2cb-115">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ba2cb-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba2cb-116">輸入</span><span class="sxs-lookup"><span data-stu-id="ba2cb-116">INPUTS</span></span>

## <span data-ttu-id="ba2cb-117">輸出</span><span class="sxs-lookup"><span data-stu-id="ba2cb-117">OUTPUTS</span></span>

### <span data-ttu-id="ba2cb-118">AzureStack. KeyVault. Quota。</span><span class="sxs-lookup"><span data-stu-id="ba2cb-118">Microsoft.AzureStack.Management.KeyVault.Admin.Models.Quota</span></span>

## <span data-ttu-id="ba2cb-119">筆記</span><span class="sxs-lookup"><span data-stu-id="ba2cb-119">NOTES</span></span>

## <span data-ttu-id="ba2cb-120">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba2cb-120">RELATED LINKS</span></span>
