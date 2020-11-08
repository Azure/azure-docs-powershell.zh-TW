---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: e9ce7a0ab98251b86990db5623b91b3a62a4cdcc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128026"
---
# <span data-ttu-id="d026d-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d026d-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="d026d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d026d-102">SYNOPSIS</span></span>
<span data-ttu-id="d026d-103">取得儲存空間帳戶的 NetWorkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="d026d-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="d026d-104">句法</span><span class="sxs-lookup"><span data-stu-id="d026d-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d026d-105">說明</span><span class="sxs-lookup"><span data-stu-id="d026d-105">DESCRIPTION</span></span>
<span data-ttu-id="d026d-106">**AzStorageAccountNetworkRuleSet** Cmdlet 會取得儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="d026d-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="d026d-107">示例</span><span class="sxs-lookup"><span data-stu-id="d026d-107">EXAMPLES</span></span>

### <span data-ttu-id="d026d-108">範例1：取得指定儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="d026d-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="d026d-109">這個命令會取得指定儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="d026d-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="d026d-110">參數</span><span class="sxs-lookup"><span data-stu-id="d026d-110">PARAMETERS</span></span>

### <span data-ttu-id="d026d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d026d-111">-DefaultProfile</span></span>
<span data-ttu-id="d026d-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d026d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d026d-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="d026d-113">-Name</span></span>
<span data-ttu-id="d026d-114">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d026d-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="d026d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d026d-115">-ResourceGroupName</span></span>
<span data-ttu-id="d026d-116">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d026d-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="d026d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d026d-117">CommonParameters</span></span>
<span data-ttu-id="d026d-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d026d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d026d-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d026d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d026d-120">輸入</span><span class="sxs-lookup"><span data-stu-id="d026d-120">INPUTS</span></span>

### <span data-ttu-id="d026d-121">System.object</span><span class="sxs-lookup"><span data-stu-id="d026d-121">System.String</span></span>

## <span data-ttu-id="d026d-122">輸出</span><span class="sxs-lookup"><span data-stu-id="d026d-122">OUTPUTS</span></span>

### <span data-ttu-id="d026d-123">PSNetworkRuleSet 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="d026d-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="d026d-124">筆記</span><span class="sxs-lookup"><span data-stu-id="d026d-124">NOTES</span></span>

## <span data-ttu-id="d026d-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="d026d-125">RELATED LINKS</span></span>
