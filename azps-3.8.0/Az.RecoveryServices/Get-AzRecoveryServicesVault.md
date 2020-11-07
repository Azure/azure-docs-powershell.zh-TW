---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: b7ee6a380bf7803913f3f302bee45bad62f106b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966162"
---
# <span data-ttu-id="f8fad-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f8fad-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="f8fad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8fad-102">SYNOPSIS</span></span>

<span data-ttu-id="f8fad-103">取得恢復服務電子倉庫的清單。</span><span class="sxs-lookup"><span data-stu-id="f8fad-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="f8fad-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8fad-104">SYNTAX</span></span>

### <span data-ttu-id="f8fad-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8fad-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8fad-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8fad-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8fad-107">說明</span><span class="sxs-lookup"><span data-stu-id="f8fad-107">DESCRIPTION</span></span>

<span data-ttu-id="f8fad-108">**AzRecoveryServicesVault** Cmdlet 會在目前的訂閱中取得恢復服務電子倉庫的清單。</span><span class="sxs-lookup"><span data-stu-id="f8fad-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="f8fad-109">示例</span><span class="sxs-lookup"><span data-stu-id="f8fad-109">EXAMPLES</span></span>

### <span data-ttu-id="f8fad-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f8fad-110">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="f8fad-111">在選取的訂閱中取得保存庫清單。</span><span class="sxs-lookup"><span data-stu-id="f8fad-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="f8fad-112">範例2</span><span class="sxs-lookup"><span data-stu-id="f8fad-112">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="f8fad-113">在 [資源群組] 中取得選取訂閱的電子倉庫清單。</span><span class="sxs-lookup"><span data-stu-id="f8fad-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="f8fad-114">範例3</span><span class="sxs-lookup"><span data-stu-id="f8fad-114">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="f8fad-115">在資源群組中取得具有指定名稱的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="f8fad-115">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="f8fad-116">參數</span><span class="sxs-lookup"><span data-stu-id="f8fad-116">PARAMETERS</span></span>

### <span data-ttu-id="f8fad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8fad-117">-DefaultProfile</span></span>

<span data-ttu-id="f8fad-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8fad-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8fad-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f8fad-119">-Name</span></span>

<span data-ttu-id="f8fad-120">指定要查詢之保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8fad-120">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8fad-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8fad-121">-ResourceGroupName</span></span>

<span data-ttu-id="f8fad-122">指定要從哪個 Azure 資源群組中檢索指定的復原服務物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8fad-122">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8fad-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="f8fad-123">-Tag</span></span>

<span data-ttu-id="f8fad-124">指定要查詢的標記</span><span class="sxs-lookup"><span data-stu-id="f8fad-124">Specifies the Tags to query for</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8fad-125">-TagName</span><span class="sxs-lookup"><span data-stu-id="f8fad-125">-TagName</span></span>

<span data-ttu-id="f8fad-126">指定要查詢的標記的索引鍵</span><span class="sxs-lookup"><span data-stu-id="f8fad-126">Specifies the Key of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8fad-127">-TagValue</span><span class="sxs-lookup"><span data-stu-id="f8fad-127">-TagValue</span></span>

<span data-ttu-id="f8fad-128">指定要查詢的標記值</span><span class="sxs-lookup"><span data-stu-id="f8fad-128">Specifies the Value of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8fad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8fad-129">CommonParameters</span></span>
<span data-ttu-id="f8fad-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8fad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8fad-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f8fad-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8fad-132">輸入</span><span class="sxs-lookup"><span data-stu-id="f8fad-132">INPUTS</span></span>

### <span data-ttu-id="f8fad-133">所有</span><span class="sxs-lookup"><span data-stu-id="f8fad-133">None</span></span>

## <span data-ttu-id="f8fad-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f8fad-134">OUTPUTS</span></span>

### <span data-ttu-id="f8fad-135">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f8fad-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="f8fad-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f8fad-136">NOTES</span></span>

## <span data-ttu-id="f8fad-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8fad-137">RELATED LINKS</span></span>

[<span data-ttu-id="f8fad-138">AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f8fad-138">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="f8fad-139">新-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f8fad-139">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="f8fad-140">移除-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f8fad-140">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
