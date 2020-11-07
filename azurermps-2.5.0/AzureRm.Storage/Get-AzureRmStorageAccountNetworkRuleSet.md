---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnetworkruleset
schema: 2.0.0
ms.openlocfilehash: 8e3aa3bd313947712ef3831b83c75bb1349adb4f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800642"
---
# <span data-ttu-id="ddf93-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ddf93-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="ddf93-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ddf93-102">SYNOPSIS</span></span>
<span data-ttu-id="ddf93-103">取得儲存空間帳戶的 NetWorkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="ddf93-103">Get the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddf93-104">句法</span><span class="sxs-lookup"><span data-stu-id="ddf93-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddf93-105">說明</span><span class="sxs-lookup"><span data-stu-id="ddf93-105">DESCRIPTION</span></span>
<span data-ttu-id="ddf93-106">**AzureRmStorageAccountNetworkRuleSet** Cmdlet 會取得儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="ddf93-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="ddf93-107">示例</span><span class="sxs-lookup"><span data-stu-id="ddf93-107">EXAMPLES</span></span>

### <span data-ttu-id="ddf93-108">範例1：取得指定儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="ddf93-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="ddf93-109">這個命令會取得指定儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="ddf93-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="ddf93-110">參數</span><span class="sxs-lookup"><span data-stu-id="ddf93-110">PARAMETERS</span></span>

### <span data-ttu-id="ddf93-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddf93-111">-DefaultProfile</span></span>
<span data-ttu-id="ddf93-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ddf93-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddf93-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="ddf93-113">-Name</span></span>
<span data-ttu-id="ddf93-114">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddf93-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="ddf93-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddf93-115">-ResourceGroupName</span></span>
<span data-ttu-id="ddf93-116">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddf93-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="ddf93-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddf93-117">CommonParameters</span></span>
<span data-ttu-id="ddf93-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ddf93-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddf93-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ddf93-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddf93-120">輸入</span><span class="sxs-lookup"><span data-stu-id="ddf93-120">INPUTS</span></span>

### <span data-ttu-id="ddf93-121">System.object</span><span class="sxs-lookup"><span data-stu-id="ddf93-121">System.String</span></span>

## <span data-ttu-id="ddf93-122">輸出</span><span class="sxs-lookup"><span data-stu-id="ddf93-122">OUTPUTS</span></span>

### <span data-ttu-id="ddf93-123">PSNetworkRuleSet 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ddf93-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="ddf93-124">筆記</span><span class="sxs-lookup"><span data-stu-id="ddf93-124">NOTES</span></span>

## <span data-ttu-id="ddf93-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddf93-125">RELATED LINKS</span></span>
