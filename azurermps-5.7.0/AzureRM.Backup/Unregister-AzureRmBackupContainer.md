---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 922BEA08-6619-4D4C-86EC-58279C9E1D93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/unregister-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
ms.openlocfilehash: 059db3658f97a28bda8960384aef4300595dca20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626555"
---
# <span data-ttu-id="508eb-101">Unregister-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="508eb-101">Unregister-AzureRmBackupContainer</span></span>

## <span data-ttu-id="508eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="508eb-102">SYNOPSIS</span></span>
<span data-ttu-id="508eb-103">從備份保存庫登出容器。</span><span class="sxs-lookup"><span data-stu-id="508eb-103">Unregisters a container from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="508eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="508eb-104">SYNTAX</span></span>

```
Unregister-AzureRmBackupContainer [-Force] [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="508eb-105">說明</span><span class="sxs-lookup"><span data-stu-id="508eb-105">DESCRIPTION</span></span>
<span data-ttu-id="508eb-106">[ **登出 AzureRmBackupContainer** ] Cmdlet 會從 Azure 備份保存庫登出 Windows Server 或 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="508eb-106">The **Unregister-AzureRmBackupContainer** cmdlet unregisters the Windows Server or Azure virtual machine from an Azure Backup vault.</span></span>
<span data-ttu-id="508eb-107">這個 Cmdlet 會從備份保存庫中移除容器的參照。</span><span class="sxs-lookup"><span data-stu-id="508eb-107">This cmdlet removes references to a container from the Backup vault.</span></span>
<span data-ttu-id="508eb-108">在您可以取消註冊容器之前，您必須刪除所有與該容器相關聯的受保護資料。</span><span class="sxs-lookup"><span data-stu-id="508eb-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

## <span data-ttu-id="508eb-109">示例</span><span class="sxs-lookup"><span data-stu-id="508eb-109">EXAMPLES</span></span>

### <span data-ttu-id="508eb-110">範例1：登出 Windows Server</span><span class="sxs-lookup"><span data-stu-id="508eb-110">Example 1: Unregister a Windows Server</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type Windows -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmBackupContainer -Container $Container[0]
Unregister Server
This operation will delete all data in the backup vault that is associated with the server. Are you sure you want to unregister the server? 
[] Yes  [] No  [?] Help (default is "No"): Yes
```

<span data-ttu-id="508eb-111">第一個命令會使用 Get-AzureRmBackupVault Cmdlet 來取得名為 Vault03 的保存庫。</span><span class="sxs-lookup"><span data-stu-id="508eb-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="508eb-112">該命令會將該物件儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="508eb-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="508eb-113">第二個命令會在 $Vault 中使用 Get-AzureRmBackupContainer Cmdlet，透過電子倉庫中的指定名稱來取得容器。</span><span class="sxs-lookup"><span data-stu-id="508eb-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="508eb-114">該命令會將該物件儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="508eb-114">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="508eb-115">最終命令會從 Azure 備份保存庫登出指定的 Windows 伺服器。</span><span class="sxs-lookup"><span data-stu-id="508eb-115">The final command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

### <span data-ttu-id="508eb-116">範例2：不需確認即取消註冊 Windows 伺服器</span><span class="sxs-lookup"><span data-stu-id="508eb-116">Example 2: Unregister a Windows Server without confirmation</span></span>
```
PS C:\>Unregister-AzureRmBackupContainer -Container $Container[0] -Force
```

<span data-ttu-id="508eb-117">這個命令會從 Azure 備份保存庫中登出指定的 Windows Server，就像第一個範例所示。</span><span class="sxs-lookup"><span data-stu-id="508eb-117">This command unregisters the specified Windows Server from the Azure Backup vault, just as in the first example.</span></span>
<span data-ttu-id="508eb-118">這個命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="508eb-118">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="508eb-119">因此，命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="508eb-119">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="508eb-120">參數</span><span class="sxs-lookup"><span data-stu-id="508eb-120">PARAMETERS</span></span>

### <span data-ttu-id="508eb-121">-容器</span><span class="sxs-lookup"><span data-stu-id="508eb-121">-Container</span></span>
<span data-ttu-id="508eb-122">指定此 Cmdlet 要取消註冊的 Windows Server 或 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="508eb-122">Specifies the Windows Server or Azure virtual machine that this cmdlet unregisters.</span></span>
<span data-ttu-id="508eb-123">若要取得 **AzureRmBackupContainer** ，請使用 Get-AzureRmBackupContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="508eb-123">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="508eb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="508eb-124">-DefaultProfile</span></span>
<span data-ttu-id="508eb-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="508eb-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="508eb-126">-Force</span><span class="sxs-lookup"><span data-stu-id="508eb-126">-Force</span></span>
<span data-ttu-id="508eb-127">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="508eb-127">Forces the command to run without asking for user confirmation.</span></span>
<span data-ttu-id="508eb-128">這個參數只適用于類型為 Windows 的 **AzureBackupContainer** 物件。</span><span class="sxs-lookup"><span data-stu-id="508eb-128">This parameter is relevant only for **AzureBackupContainer** objects of type Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="508eb-129">-確認</span><span class="sxs-lookup"><span data-stu-id="508eb-129">-Confirm</span></span>
<span data-ttu-id="508eb-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="508eb-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="508eb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="508eb-131">-WhatIf</span></span>
<span data-ttu-id="508eb-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="508eb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="508eb-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="508eb-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="508eb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="508eb-134">CommonParameters</span></span>
<span data-ttu-id="508eb-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="508eb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="508eb-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="508eb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="508eb-137">輸入</span><span class="sxs-lookup"><span data-stu-id="508eb-137">INPUTS</span></span>

### <span data-ttu-id="508eb-138">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="508eb-138">AzureBackupContainer</span></span>

## <span data-ttu-id="508eb-139">輸出</span><span class="sxs-lookup"><span data-stu-id="508eb-139">OUTPUTS</span></span>

### <span data-ttu-id="508eb-140">AzureBackupJob</span><span class="sxs-lookup"><span data-stu-id="508eb-140">AzureBackupJob</span></span>
<span data-ttu-id="508eb-141">如果容器類型是 Windows Server，此 Cmdlet 會傳回 $Null。</span><span class="sxs-lookup"><span data-stu-id="508eb-141">This cmdlet returns $Null if the container type is Windows Server.</span></span>

## <span data-ttu-id="508eb-142">筆記</span><span class="sxs-lookup"><span data-stu-id="508eb-142">NOTES</span></span>
* <span data-ttu-id="508eb-143">所有</span><span class="sxs-lookup"><span data-stu-id="508eb-143">None</span></span>

## <span data-ttu-id="508eb-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="508eb-144">RELATED LINKS</span></span>

[<span data-ttu-id="508eb-145">AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="508eb-145">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="508eb-146">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="508eb-146">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="508eb-147">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="508eb-147">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


