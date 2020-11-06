---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: cd21c9ce84a96ada003eb6520c9a2a115df186cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454723"
---
# <span data-ttu-id="158ee-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="158ee-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="158ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="158ee-102">SYNOPSIS</span></span>
<span data-ttu-id="158ee-103">變更指定池的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="158ee-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="158ee-104">句法</span><span class="sxs-lookup"><span data-stu-id="158ee-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="158ee-105">說明</span><span class="sxs-lookup"><span data-stu-id="158ee-105">DESCRIPTION</span></span>
<span data-ttu-id="158ee-106">**AzureBatchPoolOSVersion** Cmdlet 會變更指定池的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="158ee-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="158ee-107">示例</span><span class="sxs-lookup"><span data-stu-id="158ee-107">EXAMPLES</span></span>

### <span data-ttu-id="158ee-108">範例1：設定池的目標作業系統版本</span><span class="sxs-lookup"><span data-stu-id="158ee-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="158ee-109">這個命令會將 [池 MyPool] 的目標作業系統版本設定為 [WA-GUEST-OS-4.20 _201505-01]。</span><span class="sxs-lookup"><span data-stu-id="158ee-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="158ee-110">參數</span><span class="sxs-lookup"><span data-stu-id="158ee-110">PARAMETERS</span></span>

### <span data-ttu-id="158ee-111">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="158ee-111">-BatchContext</span></span>
<span data-ttu-id="158ee-112">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="158ee-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="158ee-113">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="158ee-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="158ee-114">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="158ee-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="158ee-115">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="158ee-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="158ee-116">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="158ee-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="158ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="158ee-117">-DefaultProfile</span></span>
<span data-ttu-id="158ee-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="158ee-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="158ee-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="158ee-119">-Id</span></span>
<span data-ttu-id="158ee-120">指定池的識別碼。</span><span class="sxs-lookup"><span data-stu-id="158ee-120">Specifies the ID of the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="158ee-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="158ee-121">-TargetOSVersion</span></span>
<span data-ttu-id="158ee-122">指定要在池中的虛擬機器上安裝的 Azure 客體作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="158ee-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="158ee-123">如需有關 Azure 客體作業系統版本的詳細資訊，請參閱 Azure 來賓 OS 版本與 SDK 相容性矩陣 https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) 。</span><span class="sxs-lookup"><span data-stu-id="158ee-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158ee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="158ee-124">CommonParameters</span></span>
<span data-ttu-id="158ee-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="158ee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="158ee-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="158ee-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="158ee-127">輸入</span><span class="sxs-lookup"><span data-stu-id="158ee-127">INPUTS</span></span>

### <span data-ttu-id="158ee-128">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="158ee-128">BatchAccountContext</span></span>
<span data-ttu-id="158ee-129">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="158ee-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="158ee-130">字串</span><span class="sxs-lookup"><span data-stu-id="158ee-130">String</span></span>
<span data-ttu-id="158ee-131">形參 "Id" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="158ee-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="158ee-132">輸出</span><span class="sxs-lookup"><span data-stu-id="158ee-132">OUTPUTS</span></span>

## <span data-ttu-id="158ee-133">筆記</span><span class="sxs-lookup"><span data-stu-id="158ee-133">NOTES</span></span>

## <span data-ttu-id="158ee-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="158ee-134">RELATED LINKS</span></span>

[<span data-ttu-id="158ee-135">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="158ee-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

