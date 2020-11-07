---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 25b3f15b6a71b54cbcab1a53f793a32da8b2173a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623980"
---
# <span data-ttu-id="dbc45-101">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="dbc45-101">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="dbc45-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dbc45-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc45-103">在 DevTest Labs 中取得 lab 的允許虛擬機器大小原則。</span><span class="sxs-lookup"><span data-stu-id="dbc45-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbc45-104">句法</span><span class="sxs-lookup"><span data-stu-id="dbc45-104">SYNTAX</span></span>

```
Get-AzureRmDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbc45-105">說明</span><span class="sxs-lookup"><span data-stu-id="dbc45-105">DESCRIPTION</span></span>
<span data-ttu-id="dbc45-106">**AzureRmDtlAllowedVMSizesPolicy** Cmdlet 會取得允許的虛擬機器大小原則，可讓您指定實驗室所允許的虛擬機器大小清單。</span><span class="sxs-lookup"><span data-stu-id="dbc45-106">The **Get-AzureRmDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="dbc45-107">Cmdlet 會傳回原則的啟用或停用狀態，以及您已在指定原則中設定的所有允許虛擬機器大小清單。</span><span class="sxs-lookup"><span data-stu-id="dbc45-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="dbc45-108">示例</span><span class="sxs-lookup"><span data-stu-id="dbc45-108">EXAMPLES</span></span>

## <span data-ttu-id="dbc45-109">參數</span><span class="sxs-lookup"><span data-stu-id="dbc45-109">PARAMETERS</span></span>

### <span data-ttu-id="dbc45-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc45-110">-DefaultProfile</span></span>
<span data-ttu-id="dbc45-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="dbc45-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc45-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="dbc45-112">-LabName</span></span>
<span data-ttu-id="dbc45-113">指定此 Cmdlet 取得虛擬電腦大小原則之實驗的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbc45-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="dbc45-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbc45-114">-ResourceGroupName</span></span>
<span data-ttu-id="dbc45-115">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbc45-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbc45-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc45-116">CommonParameters</span></span>
<span data-ttu-id="dbc45-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dbc45-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc45-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dbc45-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc45-119">輸入</span><span class="sxs-lookup"><span data-stu-id="dbc45-119">INPUTS</span></span>

### <span data-ttu-id="dbc45-120">所有</span><span class="sxs-lookup"><span data-stu-id="dbc45-120">None</span></span>
<span data-ttu-id="dbc45-121">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="dbc45-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dbc45-122">輸出</span><span class="sxs-lookup"><span data-stu-id="dbc45-122">OUTPUTS</span></span>

### <span data-ttu-id="dbc45-123">PSPolicy 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="dbc45-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="dbc45-124">這個 Cmdlet 會傳回指定實驗室所允許的虛擬機器大小清單的原則。</span><span class="sxs-lookup"><span data-stu-id="dbc45-124">This cmdlet returns the policy that specifies the list of virtual machine sizes allowed in the lab.</span></span>

## <span data-ttu-id="dbc45-125">筆記</span><span class="sxs-lookup"><span data-stu-id="dbc45-125">NOTES</span></span>

## <span data-ttu-id="dbc45-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbc45-126">RELATED LINKS</span></span>

[<span data-ttu-id="dbc45-127">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="dbc45-127">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Set-AzureRmDtlAllowedVMSizesPolicy.md)

[<span data-ttu-id="dbc45-128">Azure 開發測試實驗室 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dbc45-128">Azure Development Test Lab Cmdlets</span></span>](./AzureRM.DevTestLabs.md)


