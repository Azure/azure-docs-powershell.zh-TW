---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 3f38c8ace41a1f125a37053f136cd61c597787ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448438"
---
# <span data-ttu-id="3cbea-101">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="3cbea-101">Get-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="3cbea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3cbea-102">SYNOPSIS</span></span>
<span data-ttu-id="3cbea-103">取得 DevTest 實驗中實驗室的每個實驗室原則的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3cbea-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cbea-104">句法</span><span class="sxs-lookup"><span data-stu-id="3cbea-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cbea-105">說明</span><span class="sxs-lookup"><span data-stu-id="3cbea-105">DESCRIPTION</span></span>
<span data-ttu-id="3cbea-106">**AzureRmDtlVMsPerLabPolicy** Cmdlet 會取得實驗室的每個實驗室原則的虛擬機器，這可讓您設定實驗室所允許的虛擬機器總數。</span><span class="sxs-lookup"><span data-stu-id="3cbea-106">The **Get-AzureRmDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="3cbea-107">這個 Cmdlet 會傳回原則的啟用或停用狀態，以及您在原則中設定的實驗中所允許的虛擬機器總數量。</span><span class="sxs-lookup"><span data-stu-id="3cbea-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="3cbea-108">示例</span><span class="sxs-lookup"><span data-stu-id="3cbea-108">EXAMPLES</span></span>

## <span data-ttu-id="3cbea-109">參數</span><span class="sxs-lookup"><span data-stu-id="3cbea-109">PARAMETERS</span></span>

### <span data-ttu-id="3cbea-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cbea-110">-DefaultProfile</span></span>
<span data-ttu-id="3cbea-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3cbea-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cbea-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="3cbea-112">-LabName</span></span>
<span data-ttu-id="3cbea-113">指定此 Cmdlet 取得虛擬機器之實驗的名稱。</span><span class="sxs-lookup"><span data-stu-id="3cbea-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="3cbea-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cbea-114">-ResourceGroupName</span></span>
<span data-ttu-id="3cbea-115">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3cbea-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cbea-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cbea-116">CommonParameters</span></span>
<span data-ttu-id="3cbea-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3cbea-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cbea-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3cbea-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cbea-119">輸入</span><span class="sxs-lookup"><span data-stu-id="3cbea-119">INPUTS</span></span>

### <span data-ttu-id="3cbea-120">System.object</span><span class="sxs-lookup"><span data-stu-id="3cbea-120">System.String</span></span>

## <span data-ttu-id="3cbea-121">輸出</span><span class="sxs-lookup"><span data-stu-id="3cbea-121">OUTPUTS</span></span>

### <span data-ttu-id="3cbea-122">PSPolicy 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="3cbea-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="3cbea-123">筆記</span><span class="sxs-lookup"><span data-stu-id="3cbea-123">NOTES</span></span>

## <span data-ttu-id="3cbea-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="3cbea-124">RELATED LINKS</span></span>

[<span data-ttu-id="3cbea-125">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="3cbea-125">Set-AzureRmDtlVMsPerLabPolicy</span></span>](./Set-AzureRmDtlVMsPerLabPolicy.md)


