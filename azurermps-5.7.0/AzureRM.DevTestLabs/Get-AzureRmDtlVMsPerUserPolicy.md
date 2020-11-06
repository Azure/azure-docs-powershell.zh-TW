---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 53afed94f9733c041df2c49ff1ec97a2fb8277f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447809"
---
# <span data-ttu-id="bd367-101">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="bd367-101">Get-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="bd367-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd367-102">SYNOPSIS</span></span>
<span data-ttu-id="bd367-103">在 DevTest 實驗室中取得實驗室的每個使用者原則的虛擬機器原則。</span><span class="sxs-lookup"><span data-stu-id="bd367-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd367-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd367-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd367-105">說明</span><span class="sxs-lookup"><span data-stu-id="bd367-105">DESCRIPTION</span></span>
<span data-ttu-id="bd367-106">**AzureRmDtlVMsPerUserPolicy** Cmdlet 會取得實驗室的每個使用者原則的虛擬機器，這可讓您設定每位使用者允許的虛擬機器數量上限。</span><span class="sxs-lookup"><span data-stu-id="bd367-106">The **Get-AzureRmDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="bd367-107">Cmdlet 會傳回原則的啟用或停用狀態，以及您已在原則中設定的每個使用者允許的虛擬機器數量上限。</span><span class="sxs-lookup"><span data-stu-id="bd367-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="bd367-108">示例</span><span class="sxs-lookup"><span data-stu-id="bd367-108">EXAMPLES</span></span>

## <span data-ttu-id="bd367-109">參數</span><span class="sxs-lookup"><span data-stu-id="bd367-109">PARAMETERS</span></span>

### <span data-ttu-id="bd367-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd367-110">-DefaultProfile</span></span>
<span data-ttu-id="bd367-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bd367-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd367-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="bd367-112">-LabName</span></span>
<span data-ttu-id="bd367-113">指定此 Cmdlet 針對每個使用者原則取得虛擬機器原則的實驗名稱。</span><span class="sxs-lookup"><span data-stu-id="bd367-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="bd367-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd367-114">-ResourceGroupName</span></span>
<span data-ttu-id="bd367-115">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd367-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="bd367-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd367-116">CommonParameters</span></span>
<span data-ttu-id="bd367-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd367-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd367-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bd367-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd367-119">輸入</span><span class="sxs-lookup"><span data-stu-id="bd367-119">INPUTS</span></span>

### <span data-ttu-id="bd367-120">所有</span><span class="sxs-lookup"><span data-stu-id="bd367-120">None</span></span>
<span data-ttu-id="bd367-121">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="bd367-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bd367-122">輸出</span><span class="sxs-lookup"><span data-stu-id="bd367-122">OUTPUTS</span></span>

### <span data-ttu-id="bd367-123">PSPolicy 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="bd367-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="bd367-124">這個 Cmdlet 會傳回指定可由 lab 中使用者建立的虛擬機器數上限的原則。</span><span class="sxs-lookup"><span data-stu-id="bd367-124">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="bd367-125">筆記</span><span class="sxs-lookup"><span data-stu-id="bd367-125">NOTES</span></span>

## <span data-ttu-id="bd367-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd367-126">RELATED LINKS</span></span>

[<span data-ttu-id="bd367-127">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="bd367-127">Set-AzureRmDtlVMsPerUserPolicy</span></span>](./Set-AzureRmDtlVMsPerUserPolicy.md)


